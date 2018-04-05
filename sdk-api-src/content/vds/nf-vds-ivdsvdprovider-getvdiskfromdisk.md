---
UID: NF:vds.IVdsVdProvider.GetVDiskFromDisk
title: IVdsVdProvider::GetVDiskFromDisk method
author: windows-driver-content
description: Returns an IVdsVDisk interface pointer for the virtual disk given an IVdsDisk interface pointer.
old-location: base\ivdsvdprovider_getvdiskfromdisk.htm
old-project: VDS
ms.assetid: ef5fd5e0-d11f-44e1-8947-787f1e592c5c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetVDiskFromDisk method, GetVDiskFromDisk method, IVdsVdProvider interface, GetVDiskFromDisk,IVdsVdProvider.GetVDiskFromDisk, IVdsVdProvider, IVdsVdProvider interface, GetVDiskFromDisk method, IVdsVdProvider::GetVDiskFromDisk, base.ivdsvdprovider_getvdiskfromdisk, vds/IVdsVdProvider::GetVDiskFromDisk
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsVdProvider.GetVDiskFromDisk
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVdProvider::GetVDiskFromDisk method


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an <a href="https://msdn.microsoft.com/2b4f81f9-81ec-4288-a26c-8ed4d378358a">IVdsVDisk</a> interface pointer for the virtual disk given an <a href="https://msdn.microsoft.com/0fd6d1d4-daa6-4be3-8749-be98cd7c0288">IVdsDisk</a> interface pointer.


## -parameters




### -param pDisk [in]

The <a href="https://msdn.microsoft.com/2b4f81f9-81ec-4288-a26c-8ed4d378358a">IVdsVDisk</a> interface pointer for the virtual disk.


### -param ppVDisk [out]

A pointer to a variable that receives an <a href="https://msdn.microsoft.com/2b4f81f9-81ec-4288-a26c-8ed4d378358a">IVdsVDisk</a> interface pointer. Callers must release the interface pointer when it is no longer needed by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


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




<a href="https://msdn.microsoft.com/812e8ac5-91c5-455a-94e7-2edf55d92cdc">IVdsVdProvider</a>
 

 

