---
UID: NS:inked.IEC_GESTUREINFO
title: IEC_GESTUREINFO (inked.h)
description: Contains information about a specific gesture.
helpviewer_keywords: ["IEC_GESTUREINFO","IEC_GESTUREINFO (Win32 Only)","IEC_GESTUREINFO (Win32 Only) structure [Tablet PC]","f932508b-44d3-4605-97a7-bb6eed248939","inked/IEC_GESTUREINFO","tablet.iec_gestureinfo__win32_only_"]
old-location: tablet\iec_gestureinfo__win32_only_.htm
tech.root: tablet
ms.assetid: f932508b-44d3-4605-97a7-bb6eed248939
ms.date: 12/05/2018
ms.keywords: IEC_GESTUREINFO, IEC_GESTUREINFO (Win32 Only), IEC_GESTUREINFO (Win32 Only) structure [Tablet PC], f932508b-44d3-4605-97a7-bb6eed248939, inked/IEC_GESTUREINFO, tablet.iec_gestureinfo__win32_only_
req.header: inked.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEC_GESTUREINFO
 - inked/IEC_GESTUREINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - inked.h
api_name:
 - IEC_GESTUREINFO
---

# IEC_GESTUREINFO structure


## -description

Contains information about a specific gesture.

## -struct-fields

### -field nmhdr

The NMHDR structure that contains standard information about the WM_NOTIFY message. The NMHDR structure contains the handle and identifier of the control that is sending the message and the notification code, which in this case is <a href="/windows/desktop/tablet/inkedit-messages--win32-only-">IECN_GESTURE</a>. The format of the NMHDR structure is:


```cpp
typedef struct tagNMHDR {
      HWND hwndFrom;
      UINT idFrom;
      UINT code;
  } NMHDR;
```

### -field Cursor

The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> object that was used to create the gesture.

### -field Strokes

The <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that makes up the gesture.

### -field Gestures

An array of <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture">IInkGesture</a> objects, in order of confidence. For more information about this member, see the <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

## -see-also

<a href="/windows/desktop/tablet/inkedit-gesture">Gesture Event [InkEdit Control]</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture">IInkGesture Interface</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>



<a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>