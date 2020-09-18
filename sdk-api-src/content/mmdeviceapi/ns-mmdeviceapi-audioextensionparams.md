---
UID: NS:mmdeviceapi.__MIDL___MIDL_itf_mmdeviceapi_0000_0008_0001
title: AudioExtensionParams (mmdeviceapi.h)
description: This structure is passed to the Control Panel Endpoint Extension property page through IShellPropSheetExt::AddPages and is used to create endpoint PropertyPages.
helpviewer_keywords: ["AudioExtensionParams","AudioExtensionParams structure [Core Audio]","PAudioExtensionParams","PAudioExtensionParams structure pointer [Core Audio]","coreaudio.audioextensionparams","mmdeviceapi/AudioExtensionParams","mmdeviceapi/PAudioExtensionParams"]
old-location: coreaudio\audioextensionparams.htm
tech.root: CoreAudio
ms.assetid: 02A38355-104D-46C0-A34E-C0BB482323A9
ms.date: 12/05/2018
ms.keywords: AudioExtensionParams, AudioExtensionParams structure [Core Audio], PAudioExtensionParams, PAudioExtensionParams structure pointer [Core Audio], coreaudio.audioextensionparams, mmdeviceapi/AudioExtensionParams, mmdeviceapi/PAudioExtensionParams
req.header: mmdeviceapi.h
req.include-header: Mmdevapi.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: AudioExtensionParams
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mmdeviceapi_0000_0008_0001
 - mmdeviceapi/__MIDL___MIDL_itf_mmdeviceapi_0000_0008_0001
 - AudioExtensionParams
 - mmdeviceapi/AudioExtensionParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmdeviceapi.h
api_name:
 - AudioExtensionParams
---

# AudioExtensionParams structure


## -description

This structure is passed to the Control Panel Endpoint Extension property page through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages">IShellPropSheetExt::AddPages</a> and is used to create endpoint PropertyPages.

## -struct-fields

### -field AddPageParam

The add page param.

### -field pEndpoint

Pointer to the end point.

### -field pPnpInterface

Pointer to the Pnp interface.

### -field pPnpDevnode

Pointer to the Pnp devnode.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-structures">Core Audio Structures</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages">IShellPropSheetExt::AddPages</a>