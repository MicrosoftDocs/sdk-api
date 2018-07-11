---
UID: NF:vds.IVdsVDisk.GetProperties
title: IVdsVDisk::GetProperties
author: windows-sdk-content
description: Returns disk property information for the volume where the virtual disk resides.
old-location: base\ivdsvdisk_getproperties.htm
old-project: vds
ms.assetid: 0ecfbd1f-2f67-4d79-b081-7df071b070a4
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: GetProperties, GetProperties method, GetProperties method,IVdsVDisk interface, IVdsVDisk interface,GetProperties method, IVdsVDisk.GetProperties, IVdsVDisk::GetProperties, base.ivdsvdisk_getproperties, vds/IVdsVDisk::GetProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVDisk.GetProperties
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVDisk::GetProperties


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns disk property information for the volume where the virtual disk resides.


## -parameters




### -param pDiskProperties [out]

Receives a pointer to a <a href="https://msdn.microsoft.com/e4cdab29-2bb7-4754-9ac8-d6f088910b0d">VDS_VDISK_PROPERTIES</a> structure containing the disk property information.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2b4f81f9-81ec-4288-a26c-8ed4d378358a">IVdsVDisk</a>
 

 

