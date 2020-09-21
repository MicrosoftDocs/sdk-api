---
UID: NS:inked.IEC_STROKEINFO
title: IEC_STROKEINFO (inked.h)
description: Contains information about a Stroke event.
helpviewer_keywords: ["12486d28-eba2-4ef6-802e-be7155de6edd","IEC_STROKEINFO","IEC_STROKEINFO (Win32 Only)","IEC_STROKEINFO (Win32 Only) structure [Tablet PC]","inked/IEC_STROKEINFO","structure [Tablet PC]","tablet.iec_strokeinfo__win32_only_"]
old-location: tablet\iec_strokeinfo__win32_only_.htm
tech.root: tablet
ms.assetid: 12486d28-eba2-4ef6-802e-be7155de6edd
ms.date: 12/05/2018
ms.keywords: 12486d28-eba2-4ef6-802e-be7155de6edd, IEC_STROKEINFO, IEC_STROKEINFO (Win32 Only), IEC_STROKEINFO (Win32 Only) structure [Tablet PC], inked/IEC_STROKEINFO, structure [Tablet PC], tablet.iec_strokeinfo__win32_only_
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
 - IEC_STROKEINFO
 - inked/IEC_STROKEINFO
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
 - IEC_STROKEINFO
---

# IEC_STROKEINFO structure


## -description

Contains information about a <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a> event.

## -struct-fields

### -field nmhdr

Specifies the NMHDR structure that contains standard information about the WM_NOTIFY message. The NMHDR structure contains the handle and identifier of the control that is sending the message and the notification code, which in this case is <a href="/windows/desktop/tablet/inkedit-messages--win32-only-">IECN_STROKE</a>. The format of the NMHDR structure is:


```cpp
typedef struct tagNMHDR {
      HWND hwndFrom;
      UINT idFrom;
      UINT code;
  } NMHDR;
```

### -field Cursor

The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> object that was used to create the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object.

### -field Stroke

The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object that was created.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>



<a href="/windows/desktop/tablet/inkedit-stroke">Stroke Event [InkEdit Control]</a>



<a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>