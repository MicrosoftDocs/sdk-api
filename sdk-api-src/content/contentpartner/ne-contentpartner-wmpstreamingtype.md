---
UID: NE:contentpartner.WMPStreamingType
title: WMPStreamingType (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported. The WMPStreamingType enumeration specifies the type of streaming media.
helpviewer_keywords: ["WMPStreamingType","WMPStreamingType enumeration [Windows Media Player]","contentpartner/WMPStreamingType","contentpartner/wmpstMusic","contentpartner/wmpstRadio","contentpartner/wmpstUnknown","contentpartner/wmpstVideo","enumeration [Windows Media Player]","wmp.wmpstreamingtype","wmpstMusic","wmpstRadio","wmpstUnknown","wmpstVideo"]
old-location: wmp\wmpstreamingtype.htm
tech.root: WMP
ms.assetid: 3ac7e8cb-39c7-4437-a2da-6de5cb1efed9
ms.date: 12/05/2018
ms.keywords: WMPStreamingType, WMPStreamingType enumeration [Windows Media Player], contentpartner/WMPStreamingType, contentpartner/wmpstMusic, contentpartner/wmpstRadio, contentpartner/wmpstUnknown, contentpartner/wmpstVideo, enumeration [Windows Media Player], wmp.wmpstreamingtype, wmpstMusic, wmpstRadio, wmpstUnknown, wmpstVideo
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
req.typenames: WMPStreamingType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPStreamingType
 - contentpartner/WMPStreamingType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPStreamingType
---

# WMPStreamingType enumeration


## -description

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPStreamingType</b> enumeration specifies the type of streaming media.

## -enum-fields

### -field wmpstUnknown:0

Unknown type.

### -field wmpstMusic:1

The plug-in must return a URL for music content.

### -field wmpstVideo:2

The plug-in must return a URL for video content.

### -field wmpstRadio:3

The plug-in must return a URL for radio content.

## -see-also

<a href="/windows/desktop/WMP/enumerations-for-type-1-online-stores">Enumerations for Type 1 Online Stores</a>



<a href="/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl">IWMPContentPartner::GetStreamingURL</a>
