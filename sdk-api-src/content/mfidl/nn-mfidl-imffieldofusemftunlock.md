---
UID: NN:mfidl.IMFFieldOfUseMFTUnlock
title: IMFFieldOfUseMFTUnlock (mfidl.h)
description: Enables an application to use a Media Foundation transform (MFT) that has restrictions on its use.
helpviewer_keywords: ["IMFFieldOfUseMFTUnlock","IMFFieldOfUseMFTUnlock interface [Media Foundation]","IMFFieldOfUseMFTUnlock interface [Media Foundation]","described","mf.imffieldofusemftunlock","mfidl/IMFFieldOfUseMFTUnlock"]
old-location: mf\imffieldofusemftunlock.htm
tech.root: mf
ms.assetid: b144589b-d559-4686-b617-0e3c393380e9
ms.date: 12/05/2018
ms.keywords: IMFFieldOfUseMFTUnlock, IMFFieldOfUseMFTUnlock interface [Media Foundation], IMFFieldOfUseMFTUnlock interface [Media Foundation],described, mf.imffieldofusemftunlock, mfidl/IMFFieldOfUseMFTUnlock
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
 - IMFFieldOfUseMFTUnlock
 - mfidl/IMFFieldOfUseMFTUnlock
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
 - IMFFieldOfUseMFTUnlock
---

# IMFFieldOfUseMFTUnlock interface


## -description

Enables an application to use a Media Foundation transform (MFT) that has restrictions on its use.

## -inheritance

The <b>IMFFieldOfUseMFTUnlock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFFieldOfUseMFTUnlock</b> also has these types of members:

## -remarks

If you register an MFT that requires unlocking, include the <b>MFT_ENUM_FLAG_FIELDOFUSE</b> flag when you call the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a> function.

## -see-also

<a href="/windows/desktop/medfound/field-of-use-restrictions">Field of Use Restrictions</a>



<a href="/windows/desktop/medfound/mft-fieldofuse-unlock-attribute">MFT_FIELDOFUSE_UNLOCK_Attribute</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
