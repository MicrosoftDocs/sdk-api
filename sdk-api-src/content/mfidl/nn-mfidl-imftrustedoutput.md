---
UID: NN:mfidl.IMFTrustedOutput
title: IMFTrustedOutput (mfidl.h)
description: Implemented by components that provide output trust authorities (OTAs).
helpviewer_keywords: ["14342d8b-3c76-4c13-8cbe-a60bb66084c8","IMFTrustedOutput","IMFTrustedOutput interface [Media Foundation]","IMFTrustedOutput interface [Media Foundation]","described","mf.imftrustedoutput","mfidl/IMFTrustedOutput"]
old-location: mf\imftrustedoutput.htm
tech.root: mf
ms.assetid: 14342d8b-3c76-4c13-8cbe-a60bb66084c8
ms.date: 12/05/2018
ms.keywords: 14342d8b-3c76-4c13-8cbe-a60bb66084c8, IMFTrustedOutput, IMFTrustedOutput interface [Media Foundation], IMFTrustedOutput interface [Media Foundation],described, mf.imftrustedoutput, mfidl/IMFTrustedOutput
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
 - IMFTrustedOutput
 - mfidl/IMFTrustedOutput
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
 - IMFTrustedOutput
---

# IMFTrustedOutput interface


## -description

Implemented by components that provide output trust authorities (OTAs). Any Media Foundation transform (MFT) or media sink that is designed to work within the protected media path (PMP) and also sends protected content outside the Media Foundation pipeline must implement this interface.

The policy engine uses this interface to negotiate what type of content protection should be applied to the content. Applications do not use this interface directly.

## -inheritance

The <b>IMFTrustedOutput</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTrustedOutput</b> also has these types of members:

## -remarks

If an MFT supports <b>IMFTrustedOutput</b>, it must expose the interface through <b>QueryInterface</b>. The interface applies to all of the input streams on the MFT. (There is no mechanism to return a separate <b>IMFTrustedOutput</b> pointer for each stream.) The MFT must apply the  output policies to all of its input streams. If the MFT sends different streams to separate connectors, it must report all of the connector attributes.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
