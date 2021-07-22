---
UID: NN:mfidl.IMFInputTrustAuthority
title: IMFInputTrustAuthority (mfidl.h)
description: Enables other components in the protected media path (PMP) to use the input protection system provided by an input trust authorities (ITA).
helpviewer_keywords: ["637e0225-6fd8-4b83-b4fb-119e7a5ef5d2","IMFInputTrustAuthority","IMFInputTrustAuthority interface [Media Foundation]","IMFInputTrustAuthority interface [Media Foundation]","described","mf.imfinputtrustauthority","mfidl/IMFInputTrustAuthority"]
old-location: mf\imfinputtrustauthority.htm
tech.root: mf
ms.assetid: 637e0225-6fd8-4b83-b4fb-119e7a5ef5d2
ms.date: 12/05/2018
ms.keywords: 637e0225-6fd8-4b83-b4fb-119e7a5ef5d2, IMFInputTrustAuthority, IMFInputTrustAuthority interface [Media Foundation], IMFInputTrustAuthority interface [Media Foundation],described, mf.imfinputtrustauthority, mfidl/IMFInputTrustAuthority
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
 - IMFInputTrustAuthority
 - mfidl/IMFInputTrustAuthority
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
 - IMFInputTrustAuthority
---

# IMFInputTrustAuthority interface


## -description

Enables other components in the protected media path (PMP) to use the input protection system provided by an input trust authorities (ITA). An ITA is a component that implements an input protection system for media content. ITAs expose the <b>IMFInputTrustAuthority</b> interface.

An ITA translates policy from the content's native format into a common format that is used by other PMP components. It also provides a decrypter, if one is needed to decrypt the stream.

The topology contains one ITA instance for every protected stream in the media source. The ITA is obtained from the media source by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imftrustedinput-getinputtrustauthority">IMFTrustedInput::GetInputTrustAuthority</a>.

## -inheritance

The <b>IMFInputTrustAuthority</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFInputTrustAuthority</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
