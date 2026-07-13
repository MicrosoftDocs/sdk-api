---
UID: NN:mfidl.IMFOutputTrustAuthority
title: IMFOutputTrustAuthority (mfidl.h)
description: Encapsulates the functionality of one or more output protection systems that a trusted output supports.
helpviewer_keywords: ["21594ac0-7e3c-44a3-bbee-64316dd51824","IMFOutputTrustAuthority","IMFOutputTrustAuthority interface [Media Foundation]","IMFOutputTrustAuthority interface [Media Foundation]","described","mf.imfoutputtrustauthority","mfidl/IMFOutputTrustAuthority"]
old-location: mf\imfoutputtrustauthority.htm
tech.root: mf
ms.assetid: 21594ac0-7e3c-44a3-bbee-64316dd51824
ms.date: 12/05/2018
ms.keywords: 21594ac0-7e3c-44a3-bbee-64316dd51824, IMFOutputTrustAuthority, IMFOutputTrustAuthority interface [Media Foundation], IMFOutputTrustAuthority interface [Media Foundation],described, mf.imfoutputtrustauthority, mfidl/IMFOutputTrustAuthority
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFOutputTrustAuthority
 - mfidl/IMFOutputTrustAuthority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFOutputTrustAuthority
---

# IMFOutputTrustAuthority interface


## -description

Encapsulates the functionality of one or more output protection systems that a trusted output supports. This interface is exposed by output trust authority (OTA) objects. Each OTA represents a single action that the trusted output can perform, such as play, copy, or transcode. An OTA can represent more than one physical output if each output performs the same action.

## -inheritance

The <b>IMFOutputTrustAuthority</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFOutputTrustAuthority</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
