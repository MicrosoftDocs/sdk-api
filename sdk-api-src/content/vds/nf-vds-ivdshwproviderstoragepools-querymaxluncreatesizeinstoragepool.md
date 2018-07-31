---
UID: NF:vds.IVdsHwProviderStoragePools.QueryMaxLunCreateSizeInStoragePool
title: IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool
author: windows-sdk-content
description: Returns the maximum size of the LUN that can be created in the storage pool based on the specified LUN type and hints.
old-location: base\ivdshwproviderstoragepools_querymaxluncreatesizeinstoragepool.htm
old-project: VDS
ms.assetid: 37a802e2-4573-4f47-bf54-b2197034722d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVdsHwProviderStoragePools interface,QueryMaxLunCreateSizeInStoragePool method, IVdsHwProviderStoragePools.QueryMaxLunCreateSizeInStoragePool, IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool, QueryMaxLunCreateSizeInStoragePool, QueryMaxLunCreateSizeInStoragePool method, QueryMaxLunCreateSizeInStoragePool method,IVdsHwProviderStoragePools interface, base.ivdshwproviderstoragepools_querymaxluncreatesizeinstoragepool, vds/IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool, vdshwprv/IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool
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
 - IVdsHwProviderStoragePools.QueryMaxLunCreateSizeInStoragePool
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsHwProviderStoragePools::QueryMaxLunCreateSizeInStoragePool


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the maximum size of the LUN that can be created in the <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a> based on the specified LUN type and hints.


## -parameters




### -param type [in]

A <a href="https://msdn.microsoft.com/0952db7d-9dd6-4602-82d4-66d773c14463">VDS_LUN_TYPE</a> enumeration value that specifies the LUN type. This parameter is required and must be a valid LUN type.


### -param StoragePoolId [in]

A VDS_OBJECT_ID (GUID) value that identifies the storage pools to be used to create the new LUN. This parameter is required and cannot be GUID_NULL.


### -param pHints2 [in]

A pointer to a <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure that contains hints to be used in creating the LUN.


### -param pullMaxLunSize [out]

The address of a ULONGLONG value that receives the maximum LUN size, in bytes.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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




<a href="https://msdn.microsoft.com/c9db0e33-8cb1-41ba-8716-a8d70990fa3e">IVdsHwProviderStoragePools</a>
 

 

