---
UID: NN:mfidl.IMFLocalMFTRegistration
title: IMFLocalMFTRegistration (mfidl.h)
description: Registers Media Foundation transforms (MFTs) in the caller's process.
helpviewer_keywords: ["IMFLocalMFTRegistration","IMFLocalMFTRegistration interface [Media Foundation]","IMFLocalMFTRegistration interface [Media Foundation]","described","mf.imflocalmftregistration","mfidl/IMFLocalMFTRegistration"]
old-location: mf\imflocalmftregistration.htm
tech.root: mf
ms.assetid: e540a93a-ecce-4c5b-a121-b0f868a2af41
ms.date: 12/05/2018
ms.keywords: IMFLocalMFTRegistration, IMFLocalMFTRegistration interface [Media Foundation], IMFLocalMFTRegistration interface [Media Foundation],described, mf.imflocalmftregistration, mfidl/IMFLocalMFTRegistration
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFLocalMFTRegistration
 - mfidl/IMFLocalMFTRegistration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFLocalMFTRegistration
---

# IMFLocalMFTRegistration interface


## -description

Registers Media Foundation transforms (MFTs) in the caller's process.

The Media Session exposes this interface as a service. To obtain a pointer to this interface, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> method on the Media Session with the service identifier <b>MF_LOCAL_MFT_REGISTRATION_SERVICE</b>.

## -inheritance

The <b>IMFLocalMFTRegistration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFLocalMFTRegistration</b> also has these types of members:

## -remarks

This interface requires the Media Session. If you are not using the Media Session for playback, call one of the following functions instead:

<ul>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal">MFTRegisterLocal</a>
</li>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid">MFTRegisterLocalByCLSID</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
