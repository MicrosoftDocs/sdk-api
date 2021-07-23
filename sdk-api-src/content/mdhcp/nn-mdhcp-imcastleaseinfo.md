---
UID: NN:mdhcp.IMcastLeaseInfo
title: IMcastLeaseInfo (mdhcp.h)
description: The IMcastLeaseInfo interface exposes methods that can get or set information concerning a multicast address allocation. The IMcastLease object is created by calling IMcastAddressAllocation::CreateLeaseInfo.
helpviewer_keywords: ["IMcastLeaseInfo","IMcastLeaseInfo interface [TAPI 2.2]","IMcastLeaseInfo interface [TAPI 2.2]","described","_tapi3_imcastleaseinfo","mdhcp/IMcastLeaseInfo","tapi3.imcastleaseinfo"]
old-location: tapi3\imcastleaseinfo.htm
tech.root: tapi3
ms.assetid: a4ad8009-559e-4db9-9ae2-28e4d36cf346
ms.date: 12/05/2018
ms.keywords: IMcastLeaseInfo, IMcastLeaseInfo interface [TAPI 2.2], IMcastLeaseInfo interface [TAPI 2.2],described, _tapi3_imcastleaseinfo, mdhcp/IMcastLeaseInfo, tapi3.imcastleaseinfo
req.header: mdhcp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: Mdhcp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMcastLeaseInfo
 - mdhcp/IMcastLeaseInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IMcastLeaseInfo
---

# IMcastLeaseInfo interface


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IMcastLeaseInfo</b> interface exposes methods that can get or set information concerning a multicast address allocation. The IMcastLease object is created by calling 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfo">IMcastAddressAllocation::CreateLeaseInfo</a>.

## -inheritance

The <b>IMcastLeaseInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMcastLeaseInfo</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastaddressallocation">IMcastAddressAllocation</a>



<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-createleaseinfo">IMcastAddressAllocation::CreateLeaseInfo</a>



<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-renewaddress">IMcastAddressAllocation::RenewAddress</a>



<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress">IMcastAddressAllocation::RequestAddress</a>



<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a>
