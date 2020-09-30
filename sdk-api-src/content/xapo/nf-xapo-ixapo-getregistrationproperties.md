---
UID: NF:xapo.IXAPO.GetRegistrationProperties
title: IXAPO::GetRegistrationProperties (xapo.h)
description: Returns the registration properties of an XAPO.
helpviewer_keywords: ["GetRegistrationProperties","GetRegistrationProperties method [XAudio2 Audio Mixing APIs]","GetRegistrationProperties method [XAudio2 Audio Mixing APIs]","IXAPO interface","IXAPO interface [XAudio2 Audio Mixing APIs]","GetRegistrationProperties method","IXAPO.GetRegistrationProperties","IXAPO::GetRegistrationProperties","xapo/IXAPO::GetRegistrationProperties","xaudio2.ixapo_interface_getregistrationproperties"]
old-location: xaudio2\ixapo_interface_getregistrationproperties.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.GetRegistrationProperties(XAPO_REGISTRATION_PROPERTIES)
ms.date: 12/05/2018
ms.keywords: GetRegistrationProperties, GetRegistrationProperties method [XAudio2 Audio Mixing APIs], GetRegistrationProperties method [XAudio2 Audio Mixing APIs],IXAPO interface, IXAPO interface [XAudio2 Audio Mixing APIs],GetRegistrationProperties method, IXAPO.GetRegistrationProperties, IXAPO::GetRegistrationProperties, xapo/IXAPO::GetRegistrationProperties, xaudio2.ixapo_interface_getregistrationproperties
req.header: xapo.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAPO::GetRegistrationProperties
 - xapo/IXAPO::GetRegistrationProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPO.GetRegistrationProperties
---

# IXAPO::GetRegistrationProperties


## -description

Returns the registration properties of an XAPO.

## -parameters

### -param ppRegistrationProperties

Receives a pointer to a <a href="/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties">XAPO_REGISTRATION_PROPERTIES</a> structure containing the registration properties the XAPO was created with; use <a href="/windows/desktop/api/xapo/nf-xapo-xapofree">XAPOFree</a> to free the structure.

## -returns

Returns S_OK if successful; returns an error code otherwise.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a>