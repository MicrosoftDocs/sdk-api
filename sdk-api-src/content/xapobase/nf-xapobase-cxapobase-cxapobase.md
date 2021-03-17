---
UID: NF:xapobase.CXAPOBase.CXAPOBase
title: CXAPOBase::CXAPOBase (xapobase.h)
description: Creates an instance of the CXAPOBase class.
helpviewer_keywords: ["CXAPOBase","CXAPOBase interface [XAudio2 Audio Mixing APIs]","CXAPOBase method","CXAPOBase method [XAudio2 Audio Mixing APIs]","CXAPOBase method [XAudio2 Audio Mixing APIs]","CXAPOBase interface","CXAPOBase.CXAPOBase","CXAPOBase::CXAPOBase","xapobase/CXAPOBase::CXAPOBase","xaudio2.cxapobase_cxapobase"]
old-location: xaudio2\cxapobase_cxapobase.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapobase.CXAPOBase.CXAPOBase(const XAPO_REGISTRATION_PROPERTIES)
ms.date: 12/05/2018
ms.keywords: CXAPOBase, CXAPOBase interface [XAudio2 Audio Mixing APIs],CXAPOBase method, CXAPOBase method [XAudio2 Audio Mixing APIs], CXAPOBase method [XAudio2 Audio Mixing APIs],CXAPOBase interface, CXAPOBase.CXAPOBase, CXAPOBase::CXAPOBase, xapobase/CXAPOBase::CXAPOBase, xaudio2.cxapobase_cxapobase
req.header: xapobase.h
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
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CXAPOBase::CXAPOBase
 - xapobase/CXAPOBase::CXAPOBase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPOBase.lib
 - XAPOBase.dll
api_name:
 - CXAPOBase.CXAPOBase
---

# CXAPOBase::CXAPOBase


## -description

Creates an instance of the <a href="/windows/desktop/api/xapobase/nl-xapobase-cxapobase">CXAPOBase</a> class.

## -parameters

### -param pRegistrationProperties

Pointer to an <a href="/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties">XAPO_REGISTRATION_PROPERTIES</a> structure containing the registration properties for the XAPO.

## -remarks

The object created by this <a href="/windows/desktop/api/xapobase/nl-xapobase-cxapobase">CXAPOBase</a> will have a reference count of 1.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapobase/nl-xapobase-cxapobase">CXAPOBase</a>