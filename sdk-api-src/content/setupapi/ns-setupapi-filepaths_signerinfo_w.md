---
UID: NS:setupapi._FILEPATHS_SIGNERINFO_W
title: FILEPATHS_SIGNERINFO_W
author: windows-sdk-content
description: The FILEPATHS_SINGNERINFO structure stores source and target path information, and also file signature information.
old-location: setup\filepaths_signerinfo.htm
tech.root: SetupApi
ms.assetid: c651933f-cf61-4012-9d08-195336f2cb3d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PFILEPATHS_SIGNERINFO_W, FILEOP_COPY, FILEOP_DELETE, FILEPATHS_SIGNERINFO, FILEPATHS_SIGNERINFO structure [Setup API], FILEPATHS_SIGNERINFO_W, PFILEPATHS_SIGNERINFO, PFILEPATHS_SIGNERINFO structure pointer [Setup API], SP_COPY_NOBROWSE, SP_COPY_NOSKIP, SP_COPY_WARNIFSKIP, _setupapi_filepaths_signerinfo, setup.filepaths_signerinfo, setupapi/FILEPATHS_SIGNERINFO, setupapi/PFILEPATHS_SIGNERINFO"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - FILEPATHS_SIGNERINFO
product: Windows
targetos: Windows
req.typenames: FILEPATHS_SIGNERINFO_W, *PFILEPATHS_SIGNERINFO_W
req.redist: 
---

# FILEPATHS_SIGNERINFO_W structure


## -description


The <b>FILEPATHS_SINGNERINFO</b> structure stores source and target path information, and also file signature information. The setup functions send 
<b>FILEPATHS_SIGNERINFO</b> as a parameter in several of the notifications sent to callback routines. For more information, see 
<a href="https://msdn.microsoft.com/93434558-ae83-4ea2-9324-659e5873a8c3">Notifications</a>.


## -struct-fields




### -field Target

Path to the target file.


### -field Source

Path to the source file. This member is not used when the 
<a href="https://msdn.microsoft.com/220b1485-73f0-4c31-aa40-e4c9179bfd0f">FILEPATHS</a> structure is used with a file delete operation.


### -field Win32Error

If an error occurs, this member is the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. If no error has occurred, it is  NO_ERROR.


### -field Flags

Additional information that depends on the notification sent with the 
<b>FILEPATHS_SIGNERINFO</b> structure. 




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
 


### -field DigitalSigner

Digital signer of the file.


### -field Version

Version of the file.


### -field CatalogFile

Catalog file.


## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/837F1864-CE2F-4A9A-A7D9-18EB8622541E">Structures</a>
 

 

