---
UID: NF:vds.IVdsLunMpio.GetLoadBalancePolicy
title: IVdsLunMpio::GetLoadBalancePolicy (vds.h)
description: The IVdsLunMpio::GetLoadBalancePolicy method (vds.h) returns the current load balance policy on the LUN.
helpviewer_keywords: ["GetLoadBalancePolicy","GetLoadBalancePolicy method [VDS]","GetLoadBalancePolicy method [VDS]","IVdsLunMpio interface","IVdsLunMpio interface [VDS]","GetLoadBalancePolicy method","IVdsLunMpio.GetLoadBalancePolicy","IVdsLunMpio::GetLoadBalancePolicy","base.ivdslunmpio_getloadbalancepolicy","vds/IVdsLunMpio::GetLoadBalancePolicy","vdshwprv/IVdsLunMpio::GetLoadBalancePolicy"]
old-location: base\ivdslunmpio_getloadbalancepolicy.htm
tech.root: base
ms.assetid: 56866ecb-c84b-4297-9bd4-54969501bf9e
ms.date: 08/05/2022
ms.keywords: GetLoadBalancePolicy, GetLoadBalancePolicy method [VDS], GetLoadBalancePolicy method [VDS],IVdsLunMpio interface, IVdsLunMpio interface [VDS],GetLoadBalancePolicy method, IVdsLunMpio.GetLoadBalancePolicy, IVdsLunMpio::GetLoadBalancePolicy, base.ivdslunmpio_getloadbalancepolicy, vds/IVdsLunMpio::GetLoadBalancePolicy, vdshwprv/IVdsLunMpio::GetLoadBalancePolicy
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
 - IVdsLunMpio::GetLoadBalancePolicy
 - vds/IVdsLunMpio::GetLoadBalancePolicy
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
 - IVdsLunMpio.GetLoadBalancePolicy
---

# IVdsLunMpio::GetLoadBalancePolicy


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the current load balance policy on the LUN.

## -parameters

### -param pPolicy [out]

A pointer to a variable that receives an <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_loadbalance_policy_enum">VDS_LOADBALANCE_POLICY_ENUM</a> enumeration value that specifies the load balance policy.

### -param ppPaths [out]

A pointer to the array of <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_policy">VDS_PATH_POLICY</a> structures passed in by the caller. Callers must free this array by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param plNumberOfPaths [out]

A pointer to a variable that receives the number of path-specific policy information structures returned in the 
      <i>ppPaths</i> parameter.

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
The load balance policy was successfully returned. If the LUN has no paths, the array is empty, the value 
        pointed to by the  <i>plNumberOfPaths</i> parameter is set to 0, and the value pointed to 
        by the <i>ppPaths</i> parameter is set to <b>NULL</b>.

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
The cache of the provider is corrupted. This indicates a software or communication problem inside a 
        provider that caches information about the attached devices. The caller can use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
        method to  restore the cache.

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
Another operation is in progress. This operation cannot proceed until previous operations are 
        complete.

</td>
</tr>
</table>

## -remarks

The number of paths returned by this method will match the number of paths returned by 
    the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-getpathinfo">IVdsLunMpio::GetPathInfo</a> method.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslunmpio">IVdsLunMpio</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-getloadbalancepolicy">IVdsLunMpio::GetLoadBalancePolicy</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_loadbalance_policy_enum">VDS_LOADBALANCE_POLICY_ENUM</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_policy">VDS_PATH_POLICY</a>
