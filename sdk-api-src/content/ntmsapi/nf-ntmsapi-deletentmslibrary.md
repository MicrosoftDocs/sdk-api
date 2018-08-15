---
UID: NF:ntmsapi.DeleteNtmsLibrary
title: DeleteNtmsLibrary function
author: windows-sdk-content
description: The DeleteNtmsLibrary function deletes a library, and all the devices contained in the library, from the RSM database. All media in the library is moved to the offline library.
old-location: fs\deletentmslibrary.htm
old-project: Rsm
ms.assetid: 2bbc1463-9fbb-49d9-84d0-7b8ea231b454
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: DeleteNtmsLibrary, DeleteNtmsLibrary function [Files], _zaw_deletentmslibrary, base.deletentmslibrary, fs.deletentmslibrary, ntmsapi/DeleteNtmsLibrary
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - DeleteNtmsLibrary
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: ADAM
---

# DeleteNtmsLibrary function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>DeleteNtmsLibrary</b> function deletes a library, and all the devices contained in the library, from the RSM database. All media in the library is moved to the offline library.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpLibraryId [in]

Unique identifier of the library to be deleted.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
NTMS_MODIFY_ACCESS to the library is denied. Other security errors are also possible, but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database is inaccessible or damaged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FULL</b></dt>
</dl>
</td>
<td width="60%">
The database is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
The library identifier is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
There is a missing media identifier.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was an allocation failure during processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>
 




## -remarks



If the library referenced by the 
<b>DeleteNtmsLibrary</b> function contains media, the media is moved to the offline library.

You can use 
<b>DeleteNtmsLibrary</b> to remove libraries that are no longer connected to the RSM server.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb540727(v=VS.85).aspx">Library Control Functions</a>
 

 

