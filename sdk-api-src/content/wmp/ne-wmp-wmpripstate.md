---
UID: NE:wmp.WMPRipState
title: WMPRipState (wmp.h)
description: The WMPRipState enumeration type defines the possible operational states of Windows Media Player as it rips a CD.
helpviewer_keywords: ["WMPRipState","WMPRipState enumeration [Windows Media Player]","wmp.wmpripstate","wmp/WMPRipState","wmp/wmprsRipping","wmp/wmprsStopped","wmp/wmprsUnknown","wmprsRipping","wmprsStopped","wmprsUnknown"]
old-location: wmp\wmpripstate.htm
tech.root: WMP
ms.assetid: bd62cae1-3f63-4355-afc7-e429a444189d
ms.date: 12/05/2018
ms.keywords: WMPRipState, WMPRipState enumeration [Windows Media Player], wmp.wmpripstate, wmp/WMPRipState, wmp/wmprsRipping, wmp/wmprsStopped, wmp/wmprsUnknown, wmprsRipping, wmprsStopped, wmprsUnknown
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
req.typenames: WMPRipState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPRipState
 - wmp/WMPRipState
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
 - WMPRipState
---

# WMPRipState enumeration


## -description

The <b>WMPRipState</b> enumeration type defines the possible operational states of Windows Media Player as it rips a CD.

## -enum-fields

### -field wmprsUnknown:0

Not a valid state.

### -field wmprsRipping

Windows Media Player is ripping.

### -field wmprsStopped

The ripping operation is stopped.

## -remarks

Windows Media Player 10 Mobile: This enumeration is not supported.

## -see-also

<a href="/windows/desktop/WMP/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip">IWMPCdromRip Interface</a>
