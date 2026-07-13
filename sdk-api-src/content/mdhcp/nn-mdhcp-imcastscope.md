---
UID: NN:mdhcp.IMcastScope
title: IMcastScope (mdhcp.h)
description: The IMcastScope interface is obtained by calling IMcastAddressAllocation::EnumerateScopes or IMcastAddressAllocation::get_Scopes.
helpviewer_keywords: ["IMcastScope","IMcastScope interface [TAPI 2.2]","IMcastScope interface [TAPI 2.2]","described","_tapi3_imcastscope","mdhcp/IMcastScope","tapi3.imcastscope"]
old-location: tapi3\imcastscope.htm
tech.root: tapi3
ms.assetid: b0252ac4-856e-4aa7-aa3b-37b92472e864
ms.date: 12/05/2018
ms.keywords: IMcastScope, IMcastScope interface [TAPI 2.2], IMcastScope interface [TAPI 2.2],described, _tapi3_imcastscope, mdhcp/IMcastScope, tapi3.imcastscope
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
 - IMcastScope
 - mdhcp/IMcastScope
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
 - IMcastScope
---

# IMcastScope interface


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IMcastScope</b> interface is obtained by calling 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes">IMcastAddressAllocation::EnumerateScopes</a> or 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-get_scopes">IMcastAddressAllocation::get_Scopes</a>. It encapsulates all the properties of a multicast scope and provides methods to get information about the scope. This is a "read-only" interface in that it has "get" methods but no "put" methods.

## -inheritance

The <b>IMcastScope</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMcastScope</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a>
