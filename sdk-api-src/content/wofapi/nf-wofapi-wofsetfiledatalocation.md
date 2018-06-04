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

# WofSetFileDataLocation function


## -description


Used to change a file from being backed by a physical file to one backed by a system data provider.


## -parameters




### -param FileHandle [in]

A handle to a file opened with <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> or a similar API. 


### -param Provider [in]

Indicates which provider is backing this file. Currently defined providers are: 
	  	

<table>
<tr>
<td>WOF_PROVIDER_WIM</td>
<td>Indicates that the data for the file should be obtained from a WIM file.  On access, data is transparently extracted from the WIM file and provided to applications.  If the file contents are modified, data is transparently decompressed and the file is restored to the same physical form it had if this API were not used.</td>
</tr>
<tr>
<td>WOF_PROVIDER_FILE</td>
<td>Indicates that the data for the file should be compressed and stored with the file itself. On access, data is transparently decompressed and provided to applications. If the file contents are modified, data is transparently decompressed and the file is restored to the same physical form it had if this API were not used. This provider requires Windows 10.</td>
</tr>
</table>
 


### -param ExternalFileInfo [in]

Provides data specific to the specified provider. Data structures for each defined provider are: 
	  

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
 


### -param Length [in]

Specifies the length of provider specific data, in bytes. This should correspond to the structures defined above: 

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



This function returns an HRESULT indicating success or the reason for failure. 




## -remarks



When using WOF_PROVIDER_FILE, the operation may fail with ERROR_COMPRESSION_NOT_BENEFICIAL. This indicates that an attempt was made to compress the data, but no disk space was saved, so the file was not compressed. For most applications, this can be treated as a success condition.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn632443">FSCTL_SET_EXTERNAL_BACKING</a>
 

 

