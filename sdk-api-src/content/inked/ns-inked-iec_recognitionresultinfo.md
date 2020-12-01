---
UID: NS:inked.IEC_RECOGNITIONRESULTINFO
title: IEC_RECOGNITIONRESULTINFO (inked.h)
description: Contains information about an IInkRecognitionResult Interface object.
helpviewer_keywords: ["IEC_RECOGNITIONRESULTINFO","IEC_RECOGNITIONRESULTINFO (Win32 Only)","IEC_RECOGNITIONRESULTINFO (Win32 Only) structure [Tablet PC]","a17dd2e4-0649-4cfc-aab3-c032710480a1","inked/IEC_RECOGNITIONRESULTINFO","tablet.iec_recognitionresultinfo__win32_only_"]
old-location: tablet\iec_recognitionresultinfo__win32_only_.htm
tech.root: tablet
ms.assetid: a17dd2e4-0649-4cfc-aab3-c032710480a1
ms.date: 12/05/2018
ms.keywords: IEC_RECOGNITIONRESULTINFO, IEC_RECOGNITIONRESULTINFO (Win32 Only), IEC_RECOGNITIONRESULTINFO (Win32 Only) structure [Tablet PC], a17dd2e4-0649-4cfc-aab3-c032710480a1, inked/IEC_RECOGNITIONRESULTINFO, tablet.iec_recognitionresultinfo__win32_only_
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
 - IEC_RECOGNITIONRESULTINFO
 - inked/IEC_RECOGNITIONRESULTINFO
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
 - IEC_RECOGNITIONRESULTINFO
---

# IEC_RECOGNITIONRESULTINFO structure


## -description

Contains information about an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a> object.

## -struct-fields

### -field nmhdr

 The NMHDR structure that contains standard information about the WM_NOTIFY message. The NMHDR structure contains the handle and identifier of the control that is sending the message and the notification code, which in this case is <a href="/windows/desktop/tablet/inkedit-messages--win32-only-">IECN_RECOGNITIONRESULT</a>. The format of the NMHDR structure is:


```cpp
typedef struct tagNMHDR {
      HWND hwndFrom;
      UINT idFrom;
      UINT code;
  } NMHDR;
```

### -field RecognitionResult

The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult</a> object that contains recognition results.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>



<a href="/windows/desktop/tablet/inkedit-recognitionresult">RecognitionResult Event</a>



<a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>