---
UID: NE:wincodecsdk.WICMetadataCreationOptions
title: WICMetadataCreationOptions (wincodecsdk.h)
description: Specifies metadata creation options.
helpviewer_keywords: ["WICMetadataCreationAllowUnknown","WICMetadataCreationDefault","WICMetadataCreationFailUnknown","WICMetadataCreationMask","WICMetadataCreationOptions","WICMetadataCreationOptions enumeration [Windows Imaging Component]","_wic_codec_wicmetadatacreationoptions","wic._wic_codec_wicmetadatacreationoptions","wincodecsdk/WICMetadataCreationAllowUnknown","wincodecsdk/WICMetadataCreationDefault","wincodecsdk/WICMetadataCreationFailUnknown","wincodecsdk/WICMetadataCreationMask","wincodecsdk/WICMetadataCreationOptions"]
old-location: wic\_wic_codec_wicmetadatacreationoptions.htm
tech.root: wic
ms.assetid: 41fece55-1ce4-455a-99b5-5ff0ecd27e07
ms.date: 12/05/2018
ms.keywords: WICMetadataCreationAllowUnknown, WICMetadataCreationDefault, WICMetadataCreationFailUnknown, WICMetadataCreationMask, WICMetadataCreationOptions, WICMetadataCreationOptions enumeration [Windows Imaging Component], _wic_codec_wicmetadatacreationoptions, wic._wic_codec_wicmetadatacreationoptions, wincodecsdk/WICMetadataCreationAllowUnknown, wincodecsdk/WICMetadataCreationDefault, wincodecsdk/WICMetadataCreationFailUnknown, wincodecsdk/WICMetadataCreationMask, wincodecsdk/WICMetadataCreationOptions
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICMetadataCreationOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICMetadataCreationOptions
 - wincodecsdk/WICMetadataCreationOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodecsdk.h
api_name:
 - WICMetadataCreationOptions
---

# WICMetadataCreationOptions enumeration


## -description

Specifies metadata creation options.

## -enum-fields

### -field WICMetadataCreationDefault:0

The default metadata creation options. The default value is <b>WICMetadataCreationAllowUnknown</b>.

### -field WICMetadataCreationAllowUnknown

Allow unknown metadata creation.

### -field WICMetadataCreationFailUnknown:0x10000

Fail on unknown metadata creation.

### -field WICMetadataCreationMask:0xffff0000

The <a href="/windows/desktop/api/wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions">WICMetadataCreationOptions</a> mask.
