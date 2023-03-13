---
UID: NE:msvidctl.MSVidCtlStateList
title: MSVidCtlStateList (msvidctl.h)
description: This topic applies to Windows XP or later.
helpviewer_keywords: ["MSVidCtlStateList","MSVidCtlStateList enumeration [Microsoft TV Technologies]","MSVidCtlStateListEnumeration","STATE_PAUSE","STATE_PLAY","STATE_STOP","STATE_UNBUILT","enumeration [Microsoft TV Technologies]","mstv.msvidctlstatelist","msvidctl/MSVidCtlStateList","msvidctl/STATE_PAUSE","msvidctl/STATE_PLAY","msvidctl/STATE_STOP","msvidctl/STATE_UNBUILT"]
old-location: mstv\msvidctlstatelist.htm
tech.root: mstv
ms.assetid: b4da9c6e-3235-4c78-b9e1-57c9d06fccbc
ms.date: 12/05/2018
ms.keywords: MSVidCtlStateList, MSVidCtlStateList enumeration [Microsoft TV Technologies], MSVidCtlStateListEnumeration, STATE_PAUSE, STATE_PLAY, STATE_STOP, STATE_UNBUILT, enumeration [Microsoft TV Technologies], mstv.msvidctlstatelist, msvidctl/MSVidCtlStateList, msvidctl/STATE_PAUSE, msvidctl/STATE_PLAY, msvidctl/STATE_STOP, msvidctl/STATE_UNBUILT
req.header: msvidctl.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: MSVidCtlStateList
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MSVidCtlStateList
 - msvidctl/MSVidCtlStateList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msvidctl.h
api_name:
 - MSVidCtlStateList
---

# MSVidCtlStateList enumeration


## -description

This topic applies to Windows XP or later.
        



The <b>MSVidCtlStateList</b> enumeration defines the possible state values of the Video Control or the underlying filter graph.

## -enum-fields

### -field STATE_UNBUILT:-1

Indicates that there is no filter graph.

### -field STATE_STOP

Indicates that the Video Control is stopped.

### -field STATE_PAUSE

Indicates that the Video Control is paused.

### -field STATE_PLAY

Indicates that the Video Control is playing.

## -see-also

<a href="/windows/desktop/api/segment/nf-segment-imsviddeviceevent-statechange">IMSVidDeviceEvent::StateChange</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-enumerations">Video Control Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd695367(v=vs.85)">_IMSVidCtlEvents::StateChange</a>
