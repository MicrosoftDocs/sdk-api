---
UID: NS:rtscom.StylusInfo
title: StylusInfo (rtscom.h)
description: Provides information about the stylus.
helpviewer_keywords: ["StylusInfo","StylusInfo structure [Tablet PC]","d2642082-e18c-4f91-b08c-e25aa388a2a3","rtscom/StylusInfo","tablet.stylusinfo"]
old-location: tablet\stylusinfo.htm
tech.root: tablet
ms.assetid: d2642082-e18c-4f91-b08c-e25aa388a2a3
ms.date: 12/05/2018
ms.keywords: StylusInfo, StylusInfo structure [Tablet PC], d2642082-e18c-4f91-b08c-e25aa388a2a3, rtscom/StylusInfo, tablet.stylusinfo
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: StylusInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StylusInfo
 - rtscom/StylusInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RTSCom.h
api_name:
 - StylusInfo
---

# StylusInfo structure


## -description

Provides information about the stylus.

## -struct-fields

### -field tcid

Uniquely identifies the tablet.

### -field cid

Uniquely identifies the stylus.

### -field bIsInvertedCursor

<b>TRUE</b> if the stylus is upside down, otherwise <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>