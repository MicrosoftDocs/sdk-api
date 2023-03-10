---
UID: NE:msvidctl.DisplaySizeList
title: DisplaySizeList (msvidctl.h)
description: This topic applies to Windows XP or later.
helpviewer_keywords: ["DisplaySizeList","DisplaySizeList enumeration [Microsoft TV Technologies]","MSVidCtlDisplaySizeListEnumeration","dslDefaultSize","dslDoubleSourceSize","dslFullScreen","dslHalfScreen","dslHalfSourceSize","dslQuarterScreen","dslSixteenthScreen","dslSourceSize","enumeration [Microsoft TV Technologies]","mstv.displaysizelist","msvidctl/DisplaySizeList","msvidctl/dslDefaultSize","msvidctl/dslDoubleSourceSize","msvidctl/dslFullScreen","msvidctl/dslHalfScreen","msvidctl/dslHalfSourceSize","msvidctl/dslQuarterScreen","msvidctl/dslSixteenthScreen","msvidctl/dslSourceSize"]
old-location: mstv\displaysizelist.htm
tech.root: mstv
ms.assetid: 2e939cbc-fc75-41d7-9fcb-32da5173f9bc
ms.date: 12/05/2018
ms.keywords: DisplaySizeList, DisplaySizeList enumeration [Microsoft TV Technologies], MSVidCtlDisplaySizeListEnumeration, dslDefaultSize, dslDoubleSourceSize, dslFullScreen, dslHalfScreen, dslHalfSourceSize, dslQuarterScreen, dslSixteenthScreen, dslSourceSize, enumeration [Microsoft TV Technologies], mstv.displaysizelist, msvidctl/DisplaySizeList, msvidctl/dslDefaultSize, msvidctl/dslDoubleSourceSize, msvidctl/dslFullScreen, msvidctl/dslHalfScreen, msvidctl/dslHalfSourceSize, msvidctl/dslQuarterScreen, msvidctl/dslSixteenthScreen, msvidctl/dslSourceSize
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
req.typenames: DisplaySizeList
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DisplaySizeList
 - msvidctl/DisplaySizeList
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
 - DisplaySizeList
---

# DisplaySizeList enumeration


## -description

This topic applies to Windows XP or later.
        



The <b>DisplaySizeList</b> enumeration defines the possible sizes at which the video rectangle may be rendered.

## -enum-fields

### -field dslDefaultSize:0

Display the video rectangle at the native size.

### -field dslSourceSize:0

Same as <b>dslDefaultSize</b>.

### -field dslHalfSourceSize

Display the video rectangle by shrinking the width and height by half.

### -field dslDoubleSourceSize

Display the video rectangle by stretching the width and height to twice their native size.

### -field dslFullScreen

Display the video rectangle by stretching the width and height to fill the entire screen as much as possible while maintaining the original aspect ratio.

### -field dslHalfScreen

Display the video rectangle by stretching the width and height as much as possible to fill half (50%) of the screen while maintaining the original aspect ratio.

### -field dslQuarterScreen

Display the video rectangle by stretching the width and height as much as possible to fill one quarter (25%) of the screen while maintaining the original aspect ratio.

### -field dslSixteenthScreen

Display the video rectangle by stretching the width and height as much as possible to fill one sixteenth (6.25%) of the screen while maintaining the original aspect ratio.

## -see-also

<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_displaysize">IMSVidCtl::get_DisplaySize</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_displaysize">IMSVidCtl::put_DisplaySize</a>
