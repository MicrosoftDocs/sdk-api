---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WofIsExternalFile function


## -description


Used to determine if a file is being backed by a physical file or is backed by a system data provider, and optionally indicates which provider or additional data about the file.


## -parameters




### -param FilePath [in]

Specifies the path to the file for which the backing state is desired. 


### -param IsExternalFile [out, optional]

Optionally points to a BOOL value. On successful return, this value will be TRUE if the object is externally backed, FALSE if it is a physical file. 



### -param Provider [out, optional]

Optionally points to a ULONG value. On successful return, this value will be set to the provider that externally backs this object. Currently defined providers are: 
	  		

<table>
<tr>
<td>WOF_PROVIDER_WIM</td>
<td>Indicates that the data for the file resides in a separate WIM file.  On access, data is transparently extracted, decompressed and provided to applications.  If the file contents are modified, data is transparently decompressed and the file is restored to a regular file. </td>
</tr>
<tr>
<td>WOF_PROVIDER_FILE</td>
<td>Indicates that the data for the file should be compressed and stored with the file itself. On access, data is transparently decompressed and provided to applications. If the file contents are modified, data is transparently decompressed and the file is restored to a regular file. This provider requires Windows 10.</td>
</tr>
</table>
 


### -param ExternalFileInfo [out, optional]

Optionally points to a caller allocated buffer. On successful return, this buffer will contain additional information about the state of the file. If this value is provided, <b>BufferLength</b> must also be specified. Data structures for each defined provider are:
	  	

<table>
<tr>
<td>WOF_PROVIDER_WIM</td>
<td>
<a href="https://msdn.microsoft.com/BB40922B-C9D3-451C-B2D1-1740105C4BAB">WIM_EXTERNAL_FILE_INFO</a>
</td>
</tr>
<tr>
<td>WOF_PROVIDER_FILE</td>
<td>
<a href="https://msdn.microsoft.com/84FC5525-43BC-436C-AADC-C58882D48C1F">WOF_FILE_COMPRESSION_INFO</a>
</td>
</tr>
</table>
 


### -param BufferLength [in, out, optional]

Optionally points to a value that contains the length of the buffer specified in <b>ExternalFileInfo</b>. On return, this value will be set to the size of the buffer consumed, or the size of the buffer required. If the buffer is of insufficient length, this function will succeed indicating the required size and will not populate the buffer in <b>ExternalFileInfo</b>. This length should correspond to one of the structures defined above: 
	  	

<table>
<tr>
<td>WOF_PROVIDER_WIM</td>
<td>sizeof(WIM_EXTERNAL_FILE_INFO)</td>
</tr>
<tr>
<td>WOF_PROVIDER_FILE</td>
<td>sizeof(WOF_FILE_COMPRESSION_INFO)</td>
</tr>
</table>
 


## -returns



This function returns an HRESULT indicating success or the reason for failure. If the buffer specified in <i>ExternalFileInfo</i> is not of the correct size, the function will return S_OK and indicate the required buffer size in <i>BufferLength</i>. 






## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn632441">FSCTL_GET_EXTERNAL_BACKING</a>
 

 

