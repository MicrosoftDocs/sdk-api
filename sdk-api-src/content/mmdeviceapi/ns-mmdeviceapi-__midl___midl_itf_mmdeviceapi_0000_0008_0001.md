---
UID: NS:mmdeviceapi.__MIDL___MIDL_itf_mmdeviceapi_0000_0008_0001
title: "__MIDL___MIDL_itf_mmdeviceapi_0000_0008_0001"
author: windows-sdk-content
description: This structure is passed to the Control Panel Endpoint Extension property page through IShellPropSheetExt::AddPages and is used to create endpoint PropertyPages.
old-location: coreaudio\audioextensionparams.htm
tech.root: CoreAudio
ms.assetid: 02A38355-104D-46C0-A34E-C0BB482323A9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: AudioExtensionParams, AudioExtensionParams structure [Core Audio], PAudioExtensionParams, PAudioExtensionParams structure pointer [Core Audio], __MIDL___MIDL_itf_mmdeviceapi_0000_0008_0001, coreaudio.audioextensionparams, mmdeviceapi/AudioExtensionParams, mmdeviceapi/PAudioExtensionParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmdeviceapi.h
api_name:
 - AudioExtensionParams
product: Windows
targetos: Windows
req.typenames: AudioExtensionParams
req.redist: 
---

# __MIDL___MIDL_itf_mmdeviceapi_0000_0008_0001 structure


## -description


This structure is passed to the Control Panel Endpoint Extension property page through <a href="https://msdn.microsoft.com/76a2a94b-b79f-41d1-9e42-fbfda545d12f">IShellPropSheetExt::AddPages</a> and is used to create endpoint PropertyPages.


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




<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>



<a href="https://msdn.microsoft.com/76a2a94b-b79f-41d1-9e42-fbfda545d12f">IShellPropSheetExt::AddPages</a>
 

 

