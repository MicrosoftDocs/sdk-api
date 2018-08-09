---
UID: NF:vdshwprv.IVdsSubSystem2.QueryMaxLunCreateSize2
title: IVdsSubSystem2::QueryMaxLunCreateSize2
author: windows-sdk-content
description: Returns the size of the maximum LUN that can be created using the specified LUN type and hints.
old-location: base\ivdssubsystem2_querymaxluncreatesize2.htm
old-project: vds
ms.assetid: 6cd892d2-f1b0-40cd-b037-5c670da3b32f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsSubSystem2 interface,QueryMaxLunCreateSize2 method, IVdsSubSystem2.QueryMaxLunCreateSize2, IVdsSubSystem2::QueryMaxLunCreateSize2, QueryMaxLunCreateSize2, QueryMaxLunCreateSize2 method, QueryMaxLunCreateSize2 method,IVdsSubSystem2 interface, base.ivdssubsystem2_querymaxluncreatesize2, vds/IVdsSubSystem2::QueryMaxLunCreateSize2, vdshwprv/IVdsSubSystem2::QueryMaxLunCreateSize2
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsSubSystem2.QueryMaxLunCreateSize2
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsSubSystem2::QueryMaxLunCreateSize2


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the size of the maximum LUN that can be created using the specified LUN type and hints. This method is identical to the <a href="https://msdn.microsoft.com/16e8bcab-d01f-494a-9705-8392cf043674">IVdsSubSystem::QueryMaxLunCreateSize</a> method, except that the automagic hints are provided using a <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure instead of a <a href="https://msdn.microsoft.com/2c9f04bb-a014-401e-9656-affbac11f810">VDS_HINTS</a> structure.


## -parameters




### -param type [in]

A <a href="https://msdn.microsoft.com/0952db7d-9dd6-4602-82d4-66d773c14463">VDS_LUN_TYPE</a> enumeration value that specifies the LUN type.


### -param pDriveIdArray [in]

A pointer to an array containing a <b>VDS_OBJECT_ID</b> for each of the drives to be 
      used in the LUN creation. The provider should attempt to use the drives in the order provided. This parameter 
      can be <b>NULL</b> if the <i>lNumberOfDrives</i> parameter is zero, in which 
      case the provider should automatically select drives.


### -param lNumberOfDrives [in]

The number of entries in the <i>pDriveIdArray</i> array. This parameter is optional and can be zero.


### -param pHints2 [in]

A pointer to the <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure used for creating the LUN. The 
      hints always take lower priority than parameters listed before. This parameter is required and cannot be <b>NULL</b>.


### -param pullMaxLunSize [out]

A pointer to a buffer containing the maximum size of the LUN in bytes. This parameter is required and cannot be <b>NULL</b>.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
There is a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the 
        <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> method to restore 
        the cache.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The subsystem object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The subsystem is in a failed state and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or 
        operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The identifier does not refer to an existing object. This value can be returned from any method that takes a <b>VDS_OBJECT_ID</b> constant.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
This operation or combination of parameters is not supported by this provider.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7d19792c-cd37-4ea7-8830-c33c489e63e6">IVdsSubSystem2</a>



<a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a>
 

 

