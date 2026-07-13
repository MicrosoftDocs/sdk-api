---
UID: NE:wincodec.WIC8BIMIptcDigestProperties
title: WIC8BIMIptcDigestProperties (wincodec.h)
description: Specifies the identifiers of the metadata items in an 8BIM IPTC digest metadata block.
helpviewer_keywords: ["WIC8BIMIptcDigestIptcDigest","WIC8BIMIptcDigestPString","WIC8BIMIptcDigestProperties","WIC8BIMIptcDigestProperties enumeration [Windows Imaging Component]","_wic_codec_wic8bimiptcdigestproperties","wic._wic_codec_wic8bimiptcdigestproperties","wincodec/WIC8BIMIptcDigestIptcDigest","wincodec/WIC8BIMIptcDigestPString","wincodec/WIC8BIMIptcDigestProperties"]
old-location: wic\_wic_codec_wic8bimiptcdigestproperties.htm
tech.root: wic
ms.assetid: b0dbd1fa-face-4f6f-a943-60d108388b97
ms.date: 12/05/2018
ms.keywords: WIC8BIMIptcDigestIptcDigest, WIC8BIMIptcDigestPString, WIC8BIMIptcDigestProperties, WIC8BIMIptcDigestProperties enumeration [Windows Imaging Component], _wic_codec_wic8bimiptcdigestproperties, wic._wic_codec_wic8bimiptcdigestproperties, wincodec/WIC8BIMIptcDigestIptcDigest, wincodec/WIC8BIMIptcDigestPString, wincodec/WIC8BIMIptcDigestProperties
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
req.typenames: WIC8BIMIptcDigestProperties
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WIC8BIMIptcDigestProperties
 - wincodec/WIC8BIMIptcDigestProperties
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
 - WIC8BIMIptcDigestProperties
---

# WIC8BIMIptcDigestProperties enumeration


## -description

Specifies the identifiers of the metadata items in an 8BIM IPTC digest metadata block.

## -enum-fields

### -field WIC8BIMIptcDigestPString:0x1

[VT_LPSTR] A name that identifies the 8BIM block.

### -field WIC8BIMIptcDigestIptcDigest:0x2

[VT_BLOB] The embedded IPTC digest value.

### -field WIC8BIMIptcDigestProperties_FORCE_DWORD:0x7fffffff

