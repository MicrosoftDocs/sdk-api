---
UID: NS:setupapi._FILEPATHS_W
title: "_FILEPATHS_W"
author: windows-driver-content
description: The FILEPATHS structure stores source and target path information. The setup functions send the FILEPATHS structure as a parameter in several of the notifications sent to callback routines. For more information, see Notifications.
old-location: setup\filepaths_str.htm
old-project: SetupApi
ms.assetid: 220b1485-73f0-4c31-aa40-e4c9179bfd0f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PFILEPATHS_W, FILEOP_COPY, FILEOP_DELETE, FILEPATHS, FILEPATHS structure [Setup API], FILEPATHS_W, PFILEPATHS, PFILEPATHS structure pointer [Setup API], SP_COPY_NOBROWSE, SP_COPY_NOSKIP, SP_COPY_WARNIFSKIP, _FILEPATHS_W, _setupapi_filepaths_str, setup.filepaths_str, setupapi/FILEPATHS, setupapi/PFILEPATHS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: setupapi.h
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
req.typenames: FILEPATHS_W, *PFILEPATHS_W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Setupapi.h
api_name:
-	FILEPATHS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _FILEPATHS_W structure


## -description


The 
<b>FILEPATHS</b> structure stores source and target path information. The setup functions send the 
<b>FILEPATHS</b> structure as a parameter in several of the notifications sent to callback routines. For more information, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt244308">Notifications</a>.


## -struct-fields




### -field Target

Path to the target file.


### -field Source

Path to the source file. This member is not used when the 
<b>FILEPATHS</b> structure is used with a file delete operation.


### -field Win32Error

If an error occurs, this member is the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. If no error has occurred, it is  NO_ERROR.


### -field Flags

Additional information that depends on the notification sent with the 
<b>FILEPATHS</b> structure. 




For 
<a href="https://msdn.microsoft.com/d6096954-c6a5-44d4-a358-c1320c50730a">SPFILENOTIFY_COPYERROR</a> notifications, <b>Flags</b> specifies dialog box behavior and can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NOBROWSE"></a><a id="sp_copy_nobrowse"></a><dl>
<dt><b>SP_COPY_NOBROWSE</b></dt>
</dl>
</td>
<td width="60%">
Do not offer the user the option to browse.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_NOSKIP"></a><a id="sp_copy_noskip"></a><dl>
<dt><b>SP_COPY_NOSKIP</b></dt>
</dl>
</td>
<td width="60%">
Do not offer the user the option to skip the file.

</td>
</tr>
<tr>
<td width="40%"><a id="SP_COPY_WARNIFSKIP"></a><a id="sp_copy_warnifskip"></a><dl>
<dt><b>SP_COPY_WARNIFSKIP</b></dt>
</dl>
</td>
<td width="60%">
Inform the user that skipping the file may affect the installation.

</td>
</tr>
</table>
 

For 
<a href="https://msdn.microsoft.com/a0b38e2b-2390-49e5-b288-77c31636e696">SPFILENOTIFY_FILEOPDELAYED</a> notifications, <b>Flags</b> specifies the type of file operation delayed and can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILEOP_COPY"></a><a id="fileop_copy"></a><dl>
<dt><b>FILEOP_COPY</b></dt>
</dl>
</td>
<td width="60%">
A file copy operation was delayed.

</td>
</tr>
<tr>
<td width="40%"><a id="FILEOP_DELETE"></a><a id="fileop_delete"></a><dl>
<dt><b>FILEOP_DELETE</b></dt>
</dl>
</td>
<td width="60%">
A file delete operation was delayed.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

