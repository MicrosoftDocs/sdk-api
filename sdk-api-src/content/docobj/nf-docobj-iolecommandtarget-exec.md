---
UID: NF:docobj.IOleCommandTarget.Exec
title: IOleCommandTarget::Exec (docobj.h)
description: Executes the specified command or displays help for the command.
helpviewer_keywords: ["Exec","Exec method [COM]","Exec method [COM]","IOleCommandTarget interface","IOleCommandTarget interface [COM]","Exec method","IOleCommandTarget.Exec","IOleCommandTarget::Exec","_ole_iolecommandtarget_exec","com.iolecommandtarget_exec","docobj/IOleCommandTarget::Exec"]
old-location: com\iolecommandtarget_exec.htm
tech.root: com
ms.assetid: a2071ca9-8675-4f53-b30e-8c7198c2acca
ms.date: 12/05/2018
ms.keywords: Exec, Exec method [COM], Exec method [COM],IOleCommandTarget interface, IOleCommandTarget interface [COM],Exec method, IOleCommandTarget.Exec, IOleCommandTarget::Exec, _ole_iolecommandtarget_exec, com.iolecommandtarget_exec, docobj/IOleCommandTarget::Exec
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleCommandTarget::Exec
 - docobj/IOleCommandTarget::Exec
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IOleCommandTarget.Exec
---

# IOleCommandTarget::Exec


## -description

Executes the specified command or displays help for the command.

## -parameters

### -param pguidCmdGroup [in]

The unique identifier of the command group; can be <b>NULL</b> to specify the standard group.

### -param nCmdID [in]

The command to be executed. This command must belong to the group specified with <i>pguidCmdGroup</i>.

### -param nCmdexecopt [in]

Specifies how the object should execute the command. Possible values are taken from the <a href="/windows/desktop/api/docobj/ne-docobj-olecmdexecopt">OLECMDEXECOPT</a> and <a href="/windows/desktop/api/docobj/ne-docobj-olecmdid_windowstate_flag">OLECMDID_WINDOWSTATE_FLAG</a> enumerations.

### -param pvaIn [in]

A pointer to a <a href="/windows/win32/api/oaidl/ns-oaidl-variant">VARIANTARG</a> structure containing input arguments. This parameter can be <b>NULL</b>.

### -param pvaOut [in, out]

Pointer to a VARIANTARG structure to receive command output. This parameter can be <b>NULL</b>.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLECMDERR_E_UNKNOWNGROUP</b></dt>
</dl>
</td>
<td width="60%">
The <i>pguidCmdGroup</i> parameter is not <b>NULL</b> but does not specify a recognized command group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLECMDERR_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>nCmdID</i> parameter is not a valid command in the group identified by <i>pguidCmdGroup</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLECMDERR_E_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The command identified by <i>nCmdID</i> is currently disabled and cannot be executed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLECMDERR_E_NOHELP</b></dt>
</dl>
</td>
<td width="60%">
The caller has asked for help on the command identified by <i>nCmdID</i>, but no help is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLECMDERR_E_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the execution of the command.

</td>
</tr>
</table>

## -remarks

The list of input and output arguments of a command and how they are packaged is unique to each command. Such information should be documented with the specification of the command group. (See the description of OLECMDID_ZOOM in the <a href="/windows/desktop/api/docobj/ne-docobj-olecmdid">OLECMDID</a> enumeration.) In the absence of any specific information the command is assumed to take no arguments and have no return value.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The <i>pguidCmdGroup</i> and <i>nCmdID</i> parameters together uniquely identify the command to invoke. The <i>nCmdExecOpt</i> parameter specifies the exact action to be taken. (See the <a href="/windows/desktop/api/docobj/ne-docobj-olecmdexecopt">OLECMDEXECOPT</a> enumeration for more details.)

Most commands neither take arguments nor return values. For such commands, the caller can pass <b>NULL</b> in <i>pvaIn</i> and <i>pvaOut</i>. For commands that expect one or more input values, the caller can declare and initialize a VARIANTARG variable and pass a pointer to that variable in pvaIn. If the input to the command is a single value, the argument can be stored directly in the VARIANTARG structure and passed to the function. If the command expects multiple arguments, those arguments must be packaged appropriately within the VARIANTARG, using one of the supported types (such as <b>IDispatch</b> or <b>SAFEARRAY</b>).

If a command returns one or more arguments, the caller is expected to declare a VARIANTARG, initialize it to VT_EMPTY, and pass its address in pvaOut. If the command returns a single value, then the object can store that value directly in pvaOut. If the command has multiple output values, then it will package those in some way appropriate for the VARIANTARG.

Because <i>pvaIn</i> and <i>pvOut</i> are both caller-allocated, stack variables are permitted for both the caller and the object receiving the call. For commands that take zero or one argument on input and return zero or one value, no additional memory allocation is necessary. Most of the types supported by VARIANTARG do not require memory allocation. Exceptions include <b>SAFEARRAY</b> and <b>BSTR</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
A command target must implement this function; E_NOTIMPL is not a valid return value.

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-iolecommandtarget">IOleCommandTarget</a>



<a href="/windows/desktop/api/docobj/ne-docobj-olecmdexecopt">OLECMDEXECOPT</a>