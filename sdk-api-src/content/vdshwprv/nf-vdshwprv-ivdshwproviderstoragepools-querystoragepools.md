---
UID: NF:vdshwprv.IVdsHwProviderStoragePools.QueryStoragePools
title: IVdsHwProviderStoragePools::QueryStoragePools
author: windows-sdk-content
description: Returns an IEnumVdsObject enumeration object containing a list of the storage pools managed by the hardware provider.
old-location: base\ivdshwproviderstoragepools_querystoragepools.htm
tech.root: VDS
ms.assetid: 308c9821-927d-4b90-854d-b050f3730c22
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsHwProviderStoragePools interface,QueryStoragePools method, IVdsHwProviderStoragePools.QueryStoragePools, IVdsHwProviderStoragePools::QueryStoragePools, QueryStoragePools, QueryStoragePools method, QueryStoragePools method,IVdsHwProviderStoragePools interface, base.ivdshwproviderstoragepools_querystoragepools, vds/IVdsHwProviderStoragePools::QueryStoragePools, vdshwprv/IVdsHwProviderStoragePools::QueryStoragePools
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vdshwprv.h
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsHwProviderStoragePools.QueryStoragePools
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsHwProviderStoragePools::QueryStoragePools


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> enumeration object containing a list of the <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pools</a> managed by the hardware provider.


## -parameters




### -param ulFlags [in]

A bitmask of one or more <a href="https://msdn.microsoft.com/813d3452-46ad-4f7a-ab53-e3f6577b00ba">VDS_STORAGE_POOL_TYPE</a> flags that specify the types of storage pools to be queried. One of the flags must be either VDS_SPT_CONCRETE or VDS_SPT_PRIMORDIAL. The default value of this parameter is zero. A value of zero means that all storage pools should be queried.


### -param ullRemainingFreeSpace [in]

The minimum amount of free space, in bytes, that each storage pool must contain. The default value for this parameter is zero. A value of zero means that the storage pools can contain any amount of free space.


### -param pPoolAttributes [in]

A pointer to a <a href="https://msdn.microsoft.com/3dfbd3d9-ec2e-44ac-9d0f-7aa6c530db18">VDS_POOL_ATTRIBUTES</a> structure that specifies the attribute values that the returned storage pools must have. The default value for this parameter is <b>NULL</b>. A value of <b>NULL</b> means that the storage pools can have any attribute values.


### -param ppEnum [out]

The address of an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> interface 
      pointer that can be used to enumerate the storage pools. For more information, see <a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>. Callers must release the interface and each of the storage pool  objects when they are no longer needed by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.
     This parameter is required and cannot be <b>NULL</b>.


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
 




## -remarks



If the hardware provider does not manage any storage pools, this method returns an empty enumeration object.

If a non-<b>NULL</b> value is specified in the <i>pPoolAttributes</i> parameter, this method returns only storage pools that satisfy all of the attributes that are specified in the <a href="https://msdn.microsoft.com/3dfbd3d9-ec2e-44ac-9d0f-7aa6c530db18">VDS_POOL_ATTRIBUTES</a> structure. If any  minimum and maximum attributes are specified, the storage pools that are returned must match these attributes exactly. The hint attributes are used as hints to further filter the storage pools that satisfy all the specified attributes. If a specified attribute does not apply to any of the storage pools, this method returns S_OK with an empty enumeration object.




## -see-also




<a href="https://msdn.microsoft.com/c9db0e33-8cb1-41ba-8716-a8d70990fa3e">IVdsHwProviderStoragePools</a>
 

 

