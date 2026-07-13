---
UID: NS:ndattrib.tagShellCommandInfo
title: ShellCommandInfo (ndattrib.h)
description: The ShellCommandInfo structure contains data required to launch an additional application for manual repair options.
helpviewer_keywords: ["*PShellCommandInfo","ShellCommandInfo","ShellCommandInfo structure [NDF]","ShellCommandInfo","*PShellCommandInfo","ShellCommandInfo","*PShellCommandInfo structure [NDF]","ndattrib/ShellCommandInfo","ndf.shellcommandinfo"]
old-location: ndf\shellcommandinfo.htm
tech.root: NDF
ms.assetid: 54e23cfc-52bf-482a-a3e8-49fd6aa505e3
ms.date: 12/05/2018
ms.keywords: '*PShellCommandInfo, ShellCommandInfo, ShellCommandInfo structure [NDF], ShellCommandInfo,*PShellCommandInfo, ShellCommandInfo,*PShellCommandInfo structure [NDF], ndattrib/ShellCommandInfo, ndf.shellcommandinfo'
req.header: ndattrib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ndattrib.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ShellCommandInfo, *PShellCommandInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagShellCommandInfo
 - ndattrib/tagShellCommandInfo
 - PShellCommandInfo
 - ndattrib/PShellCommandInfo
 - ShellCommandInfo
 - ndattrib/ShellCommandInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndattrib.h
api_name:
 - ShellCommandInfo, *PShellCommandInfo
---

# ShellCommandInfo structure


## -description

The <b>ShellCommandInfo</b> structure contains data required to launch an additional application for manual repair options.

## -struct-fields

### -field pwszOperation

Type: <b>[string] LPWSTR</b>

A pointer to a null-terminated string that contains the action to be performed. The set of available verbs that specifies the action depends on the particular file or folder. Generally, the actions available from an object's shortcut menu are available verbs. For more information, see the Remarks section.

### -field pwszFile

Type: <b>[string] LPWSTR</b>

A pointer to a null-terminated string that specifies the file or object on which to execute the specified verb. To specify a Shell namespace object, pass the fully qualified parse name. Note that not all verbs are supported on all objects. For example, not all document types support the "print" verb.

### -field pwszParameters

Type: <b>[string] LPWSTR</b>

A pointer to a null-terminated strings that specifies the parameters to be passed to the application, only if the <i>pwszFile</i> parameter specifies an executable file. The format of this string is determined by the verb that is to be invoked. If <i>pwszFile</i> specifies a document file, <i>pwszParameters</i> should be <b>NULL</b>.

### -field pwszDirectory

Type: <b>[string] LPWSTR</b>

A pointer to a null-terminated string that specifies the default directory.

### -field nShowCmd

Type: <b>ULONG</b>

Flags that specify how an application is to be displayed when it is opened. If <i>pwszFile</i> specifies a document file, the flag is simply passed to the associated application. It is up to the application to decide how to handle it.

## -remarks

In the case of a manual repair option, the caller can use this structure to call the ShellExecute function to launch an additional application that can help the user to repair the problem.

The following verbs are used in connection with <i>pwszOperation</i>.



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="edit"></a><a id="EDIT"></a> edit

</td>
<td width="60%">
Launches an editor and opens the document for editing. If <i>pwszFile</i> is not a document file, the function fails.

</td>
</tr>
<tr>
<td width="40%">
<a id="explore"></a><a id="EXPLORE"></a> explore

</td>
<td width="60%">
Explores the folder specified by the <i>pwszFile</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<a id="find"></a><a id="FIND"></a> find

</td>
<td width="60%">
Initiates a search starting from the specified directory.

</td>
</tr>
<tr>
<td width="40%">
<a id="open"></a><a id="OPEN"></a> open

</td>
<td width="60%">
Opens the file specified by the <i>pwszFile</i> parameter. The file can be an executable file, a document file, or a folder.

</td>
</tr>
<tr>
<td width="40%">
<a id="print"></a><a id="PRINT"></a> print

</td>
<td width="60%">
Prints the document file specified by the <i>pwszFile</i> parameter. If <i>pwszFile</i> is not a document file, the function fails.

</td>
</tr>
<tr>
<td width="40%">
<a id="NULL"></a><a id="null"></a>NULL

</td>
<td width="60%">
Used when other verbs do not apply.

</td>
</tr>
</table>

