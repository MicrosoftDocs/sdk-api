---
UID: NF:vds.IVdsLunMpio.GetSupportedLbPolicies
title: IVdsLunMpio::GetSupportedLbPolicies (vds.h)
description: The IVdsLunMpio::GetSupportedLbPolicies method (vds.h) retrieves the load balance policies that are supported by the hardware provider.
helpviewer_keywords: ["GetSupportedLbPolicies","GetSupportedLbPolicies method [VDS]","GetSupportedLbPolicies method [VDS]","IVdsLunMpio interface","IVdsLunMpio interface [VDS]","GetSupportedLbPolicies method","IVdsLunMpio.GetSupportedLbPolicies","IVdsLunMpio::GetSupportedLbPolicies","base.ivdslunmpio_getsupportedlbpolicies","vds/IVdsLunMpio::GetSupportedLbPolicies","vdshwprv/IVdsLunMpio::GetSupportedLbPolicies"]
old-location: base\ivdslunmpio_getsupportedlbpolicies.htm
tech.root: base
ms.assetid: 1b1f3437-41db-403e-abdb-febbfe90858c
ms.date: 08/05/2022
ms.keywords: GetSupportedLbPolicies, GetSupportedLbPolicies method [VDS], GetSupportedLbPolicies method [VDS],IVdsLunMpio interface, IVdsLunMpio interface [VDS],GetSupportedLbPolicies method, IVdsLunMpio.GetSupportedLbPolicies, IVdsLunMpio::GetSupportedLbPolicies, base.ivdslunmpio_getsupportedlbpolicies, vds/IVdsLunMpio::GetSupportedLbPolicies, vdshwprv/IVdsLunMpio::GetSupportedLbPolicies
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
 - IVdsLunMpio::GetSupportedLbPolicies
 - vds/IVdsLunMpio::GetSupportedLbPolicies
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
 - IVdsLunMpio.GetSupportedLbPolicies
---

# IVdsLunMpio::GetSupportedLbPolicies


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves the load balance policies that are supported by the hardware provider.

## -parameters

### -param pulLbFlags [out]

The address of a <b>ULONG</b> that will receive the supported flags (as enumerated by 
      the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_provider_lbsupport_flag">VDS_PROVIDER_LBSUPPORT_FLAG</a> enumeration.)

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The load balance policy was successfully returned.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslunmpio">IVdsLunMpio</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_provider_lbsupport_flag">VDS_PROVIDER_LBSUPPORT_FLAG</a>
