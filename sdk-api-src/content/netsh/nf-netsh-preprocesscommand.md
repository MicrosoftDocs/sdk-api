---
UID: NF:netsh.PreprocessCommand
title: PreprocessCommand function (netsh.h)
description: Parses an argument string and verifies that all required tags are present.
helpviewer_keywords: ["PreprocessCommand","PreprocessCommand function [NetShell]","_netsh_preprocesscommand","netsh/PreprocessCommand","netshell.preprocesscommand"]
old-location: netshell\preprocesscommand.htm
tech.root: netshell
ms.assetid: 6795512e-4b90-47da-962a-d9e6ecfb7ee0
ms.date: 12/05/2018
ms.keywords: PreprocessCommand, PreprocessCommand function [NetShell], _netsh_preprocesscommand, netsh/PreprocessCommand, netshell.preprocesscommand
req.header: netsh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netsh.lib
req.dll: Netsh.exe
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PreprocessCommand
 - netsh/PreprocessCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netsh.exe
api_name:
 - PreprocessCommand
---

# PreprocessCommand function


## -description

The 
<b>PreprocessCommand</b> function parses an argument string and verifies that all required tags are present.

## -parameters

### -param hModule

Reserved. Set to null.

### -param ppwcArguments [in, out]

The arguments passed to 
<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-fn_handle_cmd">FN_HANDLE_CMD</a> (the command function) as its <i>ppwcArguments</i> parameter.

### -param dwCurrentIndex [in]

A value that specifies the first argument to process, such that <i>ppwcArguments</i>[<i>dwCurrentIndex</i>] is the first.

### -param dwArgCount [in]

The argument count passed as the <i>dwArgCount</i> parameter.

### -param pttTags [in]

An array of tags of type 
<b>TAG_TYPE</b>.

### -param dwTagCount [in]

 A number of entries in the <i>pttTags</i> array.

### -param dwMinArgs [in]

The minimum number of arguments required for this command.

### -param dwMaxArgs [in]

The maximum number of arguments allowed for this command.

### -param pdwTagType [out]

An array of <b>DWORD</b>s, with at least enough space for a number of entries equal to <i>dwArgCount</i> - <i>dwCurrentIndex</i>. Each <b>DWORD</b> contains the array index number in the <i>pttTags</i> array to which the array index number in the <i>ppwcArguments</i> array is matched. For example, if <i>ppwcArguments</i>[0] is matched to <i>pttTags</i>[2], <i>pdwTagType</i>[0] is 2.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
Invalid syntax.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TAG_ALREADY_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The tag is already present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was entered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_OPTION_TAG</b></dt>
</dl>
</td>
<td width="60%">
An invalid option tag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to carry out the command.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
<b>PreprocessCommand</b> function is typically called by command functions. This function parses all arguments, matching arguments with tags, and leaves the type (tag index) of each argument in the <i>pdwTagType</i> array, where <i>pdwTagType</i>[0] corresponds to the type of <i>ppwcArguments</i>[<i>dwCurrentIndex</i>]. The 
<b>PreprocessCommand</b> function also ensures that tags required to be present are present.

## -see-also

<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-fn_handle_cmd">FN_HANDLE_CMD</a>



<a href="/windows/win32/api/netsh/ns-netsh-tag_type">TAG_TYPE</a>