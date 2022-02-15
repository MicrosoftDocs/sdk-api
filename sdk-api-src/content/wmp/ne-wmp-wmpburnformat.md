---
UID: NE:wmp.WMPBurnFormat
title: WMPBurnFormat (wmp.h)
description: The WMPBurnFormat enumeration type defines the possible types of CDs for burning.
helpviewer_keywords: ["WMPBurnFormat","WMPBurnFormat enumeration [Windows Media Player]","wmp.wmpburnformat","wmp/WMPBurnFormat","wmp/wmpbfAudioCD","wmp/wmpbfDataCD","wmpbfAudioCD","wmpbfDataCD"]
old-location: wmp\wmpburnformat.htm
tech.root: WMP
ms.assetid: 5761dbfb-4e7d-4063-bde7-2aa9d7869d7c
ms.date: 12/05/2018
ms.keywords: WMPBurnFormat, WMPBurnFormat enumeration [Windows Media Player], wmp.wmpburnformat, wmp/WMPBurnFormat, wmp/wmpbfAudioCD, wmp/wmpbfDataCD, wmpbfAudioCD, wmpbfDataCD
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
req.typenames: WMPBurnFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPBurnFormat
 - wmp/WMPBurnFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPBurnFormat
---

# WMPBurnFormat enumeration


## -description

The <b>WMPBurnFormat</b> enumeration type defines the possible types of CDs for burning.

## -enum-fields

### -field wmpbfAudioCD:0

The CD being burned is an audio CD.

### -field wmpbfDataCD

The CD being burned is a data CD.

## -remarks

Windows Media Player 10 Mobile: This enumeration is not supported.

## -see-also

<a href="/windows/desktop/WMP/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnformat">IWMPCdromBurn::get_burnFormat</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat">IWMPCdromBurn::put_burnFormat</a>
