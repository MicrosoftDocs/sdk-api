---
UID: NF:ntmsapi.AddNtmsMediaType
title: AddNtmsMediaType function
author: windows-sdk-content
description: The AddNtmsMediaType function adds the specified media type to the specified library if there is not currently a relation in the library object. The function then creates the system media pools if they do not exist.
old-location: fs\addntmsmediatype.htm
tech.root: Rsm
ms.assetid: fa8ad4af-eeb8-445e-ac6c-671badb651ec
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddNtmsMediaType, AddNtmsMediaType function [Files], _zaw_addntmsmediatype, base.addntmsmediatype, fs.addntmsmediatype, ntmsapi/AddNtmsMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntmsapi.h
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - AddNtmsMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddNtmsMediaType function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>AddNtmsMediaType</b> function adds the specified media type to the specified library if there is not currently a relation in the library object. The function then creates the system 
<a href="https://msdn.microsoft.com/cad36eda-1faf-4f5b-84b8-56aa4af5f4f0">media pools</a> if they do not exist.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpMediaTypeId [in]

Unique identifier of the media type to add to the library.


### -param lpLibId [in]

Unique identifier of the library to which the media type will be added.


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
NTMS_MODIFY_ACCESS to the library is denied. Other security errors are possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b>NTMS_CONTROL_ACCESS to the library is denied. Other security errors are possible, but they would indicate a security subsystem error.

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
The library ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
The media type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The media type or library ID is missing.

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
 




## -see-also




<a href="https://msdn.microsoft.com/c2a2bc8a-4230-44c4-b6bc-4b4e2a9fece1">DeleteNtmsMediaType</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb540727(v=VS.85).aspx">Media Services Functions</a>
 

 

