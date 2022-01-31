---
UID: NE:wincodec.WICPngIccpProperties
title: WICPngIccpProperties (wincodec.h)
description: Specifies the Portable Network Graphics (PNG) iCCP chunk metadata properties.
helpviewer_keywords: ["WICPngIccpProfileData","WICPngIccpProfileName","WICPngIccpProperties","WICPngIccpProperties enumeration [Windows Imaging Component]","_wic_codec_wicpngiccpproperties","wic._wic_codec_wicpngiccpproperties","wincodec/WICPngIccpProfileData","wincodec/WICPngIccpProfileName","wincodec/WICPngIccpProperties"]
old-location: wic\_wic_codec_wicpngiccpproperties.htm
tech.root: wic
ms.assetid: 2c28a4f1-40c2-4886-be5f-0a2e6feb487a
ms.date: 12/05/2018
ms.keywords: WICPngIccpProfileData, WICPngIccpProfileName, WICPngIccpProperties, WICPngIccpProperties enumeration [Windows Imaging Component], _wic_codec_wicpngiccpproperties, wic._wic_codec_wicpngiccpproperties, wincodec/WICPngIccpProfileData, wincodec/WICPngIccpProfileName, wincodec/WICPngIccpProperties
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICPngIccpProperties
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICPngIccpProperties
 - wincodec/WICPngIccpProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICPngIccpProperties
---

# WICPngIccpProperties enumeration


## -description

Specifies the Portable Network Graphics (PNG) iCCP chunk metadata properties.

## -enum-fields

### -field WICPngIccpProfileName:0x1

[VT_LPSTR] Indicates the International Color Consortium (ICC) profile name.

### -field WICPngIccpProfileData:0x2

[VT_VECTOR \| VT_UI1] Indicates the embedded ICC profile.

### -field WICPngIccpProperties_FORCE_DWORD:0x7fffffff

