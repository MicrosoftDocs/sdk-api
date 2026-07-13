---
UID: NF:vds.IVdsLunIscsi.AssociateTargets
title: IVdsLunIscsi::AssociateTargets (vds.h)
description: The IVdsLunIscsi::AssociateTargets method (vds.h) associates LUNs with subsystem iSCSI targets.
helpviewer_keywords: ["AssociateTargets","AssociateTargets method [VDS]","AssociateTargets method [VDS]","IVdsLunIscsi interface","IVdsLunIscsi interface [VDS]","AssociateTargets method","IVdsLunIscsi.AssociateTargets","IVdsLunIscsi::AssociateTargets","base.ivdsluniscsi_associatetargets","vds/IVdsLunIscsi::AssociateTargets","vdshwprv/IVdsLunIscsi::AssociateTargets"]
old-location: base\ivdsluniscsi_associatetargets.htm
tech.root: base
ms.assetid: eb80020b-caf8-4d85-b250-d9a8738b8848
ms.date: 08/05/2022
ms.keywords: AssociateTargets, AssociateTargets method [VDS], AssociateTargets method [VDS],IVdsLunIscsi interface, IVdsLunIscsi interface [VDS],AssociateTargets method, IVdsLunIscsi.AssociateTargets, IVdsLunIscsi::AssociateTargets, base.ivdsluniscsi_associatetargets, vds/IVdsLunIscsi::AssociateTargets, vdshwprv/IVdsLunIscsi::AssociateTargets
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsLunIscsi::AssociateTargets
 - vds/IVdsLunIscsi::AssociateTargets
dev_langs:
 - c++
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
---

# IVdsLunIscsi::AssociateTargets


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Associates LUNs with subsystem iSCSI targets.

## -parameters

### -param pTargetIdArray [in]

A pointer to an array of target <b>VDS_OBJECT_ID</b> data types. The provider 
      associates these iSCSI targets with the LUN. This array includes targets already associated with the LUN that 
      are to remain so.

### -param lNumberOfTargets [in]

The number of targets specified in the <i>pTargetArray</i> parameter.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method
        followed by the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to restore 
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
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsluniscsi-queryassociatedtargets">IVdsLunIscsi::QueryAssociatedTargets</a> 
    method to query target associations. Use the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-queryassociatedluns">IVdsIscsiTarget::QueryAssociatedLuns</a> 
    method to query the LUNs associated with a target.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsluniscsi">IVdsLunIscsi</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsluniscsi-queryassociatedtargets">IVdsLunIscsi::QueryAssociatedTargets</a>
