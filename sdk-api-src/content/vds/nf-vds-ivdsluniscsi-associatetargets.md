---
UID: NF:vds.IVdsLunIscsi.AssociateTargets
title: IVdsLunIscsi::AssociateTargets
author: windows-sdk-content
description: Associates LUNs with subsystem iSCSI targets.
old-location: base\ivdsluniscsi_associatetargets.htm
old-project: VDS
ms.assetid: eb80020b-caf8-4d85-b250-d9a8738b8848
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: AssociateTargets, AssociateTargets method [VDS], AssociateTargets method [VDS],IVdsLunIscsi interface, IVdsLunIscsi interface [VDS],AssociateTargets method, IVdsLunIscsi.AssociateTargets, IVdsLunIscsi::AssociateTargets, base.ivdsluniscsi_associatetargets, vds/IVdsLunIscsi::AssociateTargets, vdshwprv/IVdsLunIscsi::AssociateTargets
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - Vds.h
 - VdsHwPrv.h
api_name:
 - IVdsLunIscsi.AssociateTargets
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsLunIscsi::AssociateTargets


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Associates LUNs with subsystem iSCSI targets.


## -parameters




### -param pTargetIdArray [in]

A pointer to an array of target <b>VDS_OBJECT_ID</b> data types. The provider 
      associates these iSCSI targets with the LUN. This array includes targets already associated with the LUN that 
      are to remain so.


### -param lNumberOfTargets [in]

The number of targets specified in the <i>pTargetArray</i> parameter.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
This return value signals a software or communication problem inside a provider that caches information 
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
The LUN object is no longer present.

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
The LUN is in a failed state, and is unable to perform the requested operation.

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
Can be returned from any method that takes a <b>VDS_OBJECT_ID</b> constant. This return 
        value indicates that the identifier does not refer to an existing object.

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
 




## -remarks



Most subsystems implement only one associated target per LUN, but some allow for multiple associated 
    targets.

Use the 
    <a href="https://msdn.microsoft.com/4979e3c1-d966-4dfd-bb87-73c3e1252c50">IVdsLunIscsi::QueryAssociatedTargets</a> 
    method to query target associations. Use the 
    <a href="https://msdn.microsoft.com/3f375c0b-7400-4660-8cb1-5291fd0dd52c">IVdsIscsiTarget::QueryAssociatedLuns</a> 
    method to query the LUNs associated with a target.




## -see-also




<a href="https://msdn.microsoft.com/5b1e6204-6cc0-4d94-8e54-fa963f83ae39">IVdsLunIscsi</a>



<a href="https://msdn.microsoft.com/4979e3c1-d966-4dfd-bb87-73c3e1252c50">IVdsLunIscsi::QueryAssociatedTargets</a>
 

 

