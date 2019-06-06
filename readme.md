<!--
This file was generate by MarkdownSnippets.
Source File: /readme.source.md
To change this file edit the source file and then re-run the generation using either the dotnet global tool (https://github.com/SimonCropp/MarkdownSnippets#githubmarkdownsnippets) or using the api (https://github.com/SimonCropp/MarkdownSnippets#running-as-a-unit-test).
-->
# <img src="https://avatars3.githubusercontent.com/u/36907" height="30px"> ApprovalTests.WinForms

Extends [ApprovalTests](https://github.com/approvals/ApprovalTests.Net) for approval of Windows Forms through screenshot verification.


## The NuGet package [![NuGet Status](http://img.shields.io/nuget/v/ApprovalTests.WinForms.svg?style=flat)](https://www.nuget.org/packages/ApprovalTests.WinForms/)

https://nuget.org/packages/ApprovalTests.WinForms/

    PM> Install-Package ApprovalTests.WinForms


## Usage


<!-- snippet: usage -->
```cs
WinFormsApprovals.Verify(new Form());
```
<sup>[snippet source](/src/Tests/WinFormTests.cs#L52-L56)</sup>
<!-- endsnippet -->

## System Differences

Usually Approval files take the form 

`ClassName.MethodName.approved.extention` 

However, as winforms will render differently on each OS, when approving with winform it will take the form

`ClassName.MethodName.osname.approved.extention` 

It does this before each run by calling  

<!-- snippet: additional_info -->
```cs
ApprovalResults.UniqueForOs;
```
<sup>[snippet source](/src/ApprovalTests.WinForms/WinFormsApprovals.cs#L15-L17)</sup>
<!-- endsnippet -->


An Example Approval File would be:

`WinFormTests.TestControlApproved.Microsoft_Windows_10_Home_N.approved.png`

### Customizing System Naming

If you would like a diffent naming system you can customize the default naming.
For example, if you would like to use the .net_version number you could do this:

<!-- snippet: alternative_naming -->
** Could not find snippet 'alternative_naming' **

Would yield:

<!-- snippet: alternative_custom_name -->
** Could not find snippet 'alternative_custom_name' **


## Links

 * NuGet: https://nuget.org/packages/ApprovalTests.WinForms/
 * Build: [![Build Status](https://dev.azure.com/approvals/ApprovalTests.Net.WinForms/_apis/build/status/approvals.ApprovalTests.Net.WinForms?branchName=master)](https://dev.azure.com/approvals/ApprovalTests.Net.WinForms/_build/latest?definitionId=2&branchName=master)
