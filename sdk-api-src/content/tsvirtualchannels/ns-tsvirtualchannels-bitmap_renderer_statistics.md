---
UID: NS:tsvirtualchannels.__BITMAP_RENDERER_STATISTICS
title: BITMAP_RENDERER_STATISTICS (tsvirtualchannels.h)
description: Contains statistics for the RemoteFX media redirection bitmap renderer.
helpviewer_keywords: ["*PBITMAP_RENDERER_STATISTICS","BITMAP_RENDERER_STATISTICS","BITMAP_RENDERER_STATISTICS structure [Remote Desktop Services]","PBITMAP_RENDERER_STATISTICS","PBITMAP_RENDERER_STATISTICS structure pointer [Remote Desktop Services]","termserv.bitmap_renderer_statistics","tsvirtualchannels/BITMAP_RENDERER_STATISTICS","tsvirtualchannels/PBITMAP_RENDERER_STATISTICS"]
old-location: termserv\bitmap_renderer_statistics.htm
tech.root: TermServ
ms.assetid: 111FA0B3-BFC1-4BD7-8BF0-C0C746A39C5D
ms.date: 12/05/2018
ms.keywords: '*PBITMAP_RENDERER_STATISTICS, BITMAP_RENDERER_STATISTICS, BITMAP_RENDERER_STATISTICS structure [Remote Desktop Services], PBITMAP_RENDERER_STATISTICS, PBITMAP_RENDERER_STATISTICS structure pointer [Remote Desktop Services], termserv.bitmap_renderer_statistics, tsvirtualchannels/BITMAP_RENDERER_STATISTICS, tsvirtualchannels/PBITMAP_RENDERER_STATISTICS'
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSVirtualChannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __BITMAP_RENDERER_STATISTICS
 - tsvirtualchannels/__BITMAP_RENDERER_STATISTICS
 - PBITMAP_RENDERER_STATISTICS
 - tsvirtualchannels/PBITMAP_RENDERER_STATISTICS
 - BITMAP_RENDERER_STATISTICS
 - tsvirtualchannels/BITMAP_RENDERER_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tsvirtualchannels.h
api_name:
 - BITMAP_RENDERER_STATISTICS
---

# BITMAP_RENDERER_STATISTICS structure


## -description

Contains statistics for the RemoteFX media redirection bitmap renderer.

## -struct-fields

### -field dwFramesDelivered

The number of frames delivered.

### -field dwFramesDropped

The number of frames dropped.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsbitmaprenderer-getrendererstatistics">GetRendererStatistics</a>