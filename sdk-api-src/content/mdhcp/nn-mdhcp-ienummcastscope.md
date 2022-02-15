---
UID: NN:mdhcp.IEnumMcastScope
title: IEnumMcastScope (mdhcp.h)
description: The IEnumMcastScope interface provides COM-standard enumeration methods for the IMcastScope interface. The IMcastAddressAllocation::EnumerateScopes method returns a pointer to IEnumMcastScope.
helpviewer_keywords: ["IEnumMcastScope","IEnumMcastScope interface [TAPI 2.2]","IEnumMcastScope interface [TAPI 2.2]","described","_tapi3_ienummcastscope","mdhcp/IEnumMcastScope","tapi3.ienummcastscope"]
old-location: tapi3\ienummcastscope.htm
tech.root: tapi3
ms.assetid: edc8be8e-635b-43f3-a4c1-7566e354cc3e
ms.date: 12/05/2018
ms.keywords: IEnumMcastScope, IEnumMcastScope interface [TAPI 2.2], IEnumMcastScope interface [TAPI 2.2],described, _tapi3_ienummcastscope, mdhcp/IEnumMcastScope, tapi3.ienummcastscope
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
 - IEnumMcastScope
 - mdhcp/IEnumMcastScope
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
 - IEnumMcastScope
---

# IEnumMcastScope interface


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IEnumMcastScope</b> interface provides COM-standard enumeration methods for the 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a> interface. The 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes">IMcastAddressAllocation::EnumerateScopes</a> method returns a pointer to 
<b>IEnumMcastScope</b>.

## -inheritance

The <b>IEnumMcastScope</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumMcastScope</b> also has these types of members:

