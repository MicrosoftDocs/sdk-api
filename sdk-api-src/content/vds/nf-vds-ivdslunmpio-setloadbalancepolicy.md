---
UID: NF:vds.IVdsLunMpio.SetLoadBalancePolicy
title: IVdsLunMpio::SetLoadBalancePolicy (vds.h)
description: The IVdsLunMpio::SetLoadBalancePolicy method (vds.h) sets the load balance policy on the LUN.
helpviewer_keywords: ["IVdsLunMpio interface [VDS]","SetLoadBalancePolicy method","IVdsLunMpio.SetLoadBalancePolicy","IVdsLunMpio::SetLoadBalancePolicy","SetLoadBalancePolicy","SetLoadBalancePolicy method [VDS]","SetLoadBalancePolicy method [VDS]","IVdsLunMpio interface","base.ivdslunmpio_setloadbalancepolicy","vds/IVdsLunMpio::SetLoadBalancePolicy","vdshwprv/IVdsLunMpio::SetLoadBalancePolicy"]
old-location: base\ivdslunmpio_setloadbalancepolicy.htm
tech.root: base
ms.assetid: 2f3eb00a-864e-4fb7-a722-4537e6b8dd42
ms.date: 08/05/2022
ms.keywords: IVdsLunMpio interface [VDS],SetLoadBalancePolicy method, IVdsLunMpio.SetLoadBalancePolicy, IVdsLunMpio::SetLoadBalancePolicy, SetLoadBalancePolicy, SetLoadBalancePolicy method [VDS], SetLoadBalancePolicy method [VDS],IVdsLunMpio interface, base.ivdslunmpio_setloadbalancepolicy, vds/IVdsLunMpio::SetLoadBalancePolicy, vdshwprv/IVdsLunMpio::SetLoadBalancePolicy
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsLunMpio::SetLoadBalancePolicy
 - vds/IVdsLunMpio::SetLoadBalancePolicy
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
 - IVdsLunMpio.SetLoadBalancePolicy
---

# IVdsLunMpio::SetLoadBalancePolicy


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the load balance policy on the LUN.

## -parameters

### -param policy

The load balance policy enumerated by the  
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_loadbalance_policy_enum">VDS_LOADBALANCE_POLICY_ENUM</a> enumeration.

### -param pPaths

A 
      pointer to an array of members of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_policy">VDS_PATH_POLICY</a> structure 
      that contain the path-specific policy information.

### -param lNumberOfPaths

The number of members of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_policy">VDS_PATH_POLICY</a> structure in the array 
      pointed to by the <i>pPaths</i> parameter.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The load balance policy was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to 
        restore the cache.
       

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
The LUN is in a failed state and is unable to perform the requested operation.

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
Another operation is in progress. This operation cannot proceed until previous operations are complete.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslunmpio">IVdsLunMpio</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-getloadbalancepolicy">IVdsLunMpio::GetLoadBalancePolicy</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_loadbalance_policy_enum">VDS_LOADBALANCE_POLICY_ENUM</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_policy">VDS_PATH_POLICY</a>
