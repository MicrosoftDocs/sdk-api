---
UID: NE:wincodec.WIC8BIMIptcProperties
title: WIC8BIMIptcProperties (wincodec.h)
description: Specifies the identifiers of the metadata items in an 8BIM IPTC block.
helpviewer_keywords: ["WIC8BIMEmbeddedIPTC","WIC8BIMIptcPString","WIC8BIMIptcProperties","WIC8BIMIptcProperties enumeration [Windows Imaging Component]","_wic_codec_wic8bimiptcproperties","wic._wic_codec_wic8bimiptcproperties","wincodec/WIC8BIMEmbeddedIPTC","wincodec/WIC8BIMIptcPString","wincodec/WIC8BIMIptcProperties"]
old-location: wic\_wic_codec_wic8bimiptcproperties.htm
tech.root: wic
ms.assetid: c752790c-6392-4406-b006-8f5da9f4e23d
ms.date: 12/05/2018
ms.keywords: WIC8BIMEmbeddedIPTC, WIC8BIMIptcPString, WIC8BIMIptcProperties, WIC8BIMIptcProperties enumeration [Windows Imaging Component], _wic_codec_wic8bimiptcproperties, wic._wic_codec_wic8bimiptcproperties, wincodec/WIC8BIMEmbeddedIPTC, wincodec/WIC8BIMIptcPString, wincodec/WIC8BIMIptcProperties
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
req.typenames: WIC8BIMIptcProperties
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WIC8BIMIptcProperties
 - wincodec/WIC8BIMIptcProperties
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
 - WIC8BIMIptcProperties
---

# WIC8BIMIptcProperties enumeration


## -description

Specifies the identifiers of the metadata items in an 8BIM IPTC block.

## -enum-fields

### -field WIC8BIMIptcPString:0

[VT_LPSTR] A name that identifies the 8BIM block.

### -field WIC8BIMIptcEmbeddedIPTC:0x1

### -field WIC8BIMIptcProperties_FORCE_DWORD:0x7fffffff

#### - WIC8BIMEmbeddedIPTC

[VT_UNKNOWN] The IPTC block embedded in this 8BIM IPTC block.

