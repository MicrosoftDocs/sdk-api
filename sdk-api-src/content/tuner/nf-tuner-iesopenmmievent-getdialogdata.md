---
UID: NF:tuner.IESOpenMmiEvent.GetDialogData
title: IESOpenMmiEvent::GetDialogData (tuner.h)
description: Gets the data associated with an OpenMMI event, in byte stream format. This data can be the contents of the dialog that is opened or the Uniform Resource Locator (URL) that contains the dialog.
helpviewer_keywords: ["GetDialogData","GetDialogData method [Microsoft TV Technologies]","GetDialogData method [Microsoft TV Technologies]","IESOpenMmiEvent interface","IESOpenMmiEvent interface [Microsoft TV Technologies]","GetDialogData method","IESOpenMmiEvent.GetDialogData","IESOpenMmiEvent::GetDialogData","mstv.iesopenmmievent_getdialogdata","tuner/IESOpenMmiEvent::GetDialogData"]
old-location: mstv\iesopenmmievent_getdialogdata.htm
tech.root: mstv
ms.assetid: c5deaffb-ceac-4609-a862-b050a1afa1f9
ms.date: 12/05/2018
ms.keywords: GetDialogData, GetDialogData method [Microsoft TV Technologies], GetDialogData method [Microsoft TV Technologies],IESOpenMmiEvent interface, IESOpenMmiEvent interface [Microsoft TV Technologies],GetDialogData method, IESOpenMmiEvent.GetDialogData, IESOpenMmiEvent::GetDialogData, mstv.iesopenmmievent_getdialogdata, tuner/IESOpenMmiEvent::GetDialogData
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IESOpenMmiEvent::GetDialogData
 - tuner/IESOpenMmiEvent::GetDialogData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESOpenMmiEvent.GetDialogData
---

# IESOpenMmiEvent::GetDialogData


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the data associated with an <b>OpenMMI</b> event, in byte stream format. This data can be the contents of the dialog that is opened or the Uniform Resource Locator (URL) that contains the dialog.

## -parameters

### -param pbData [out, retval]

Pointer to a SAFEARRAY object containing the event data. 
          
          The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesopenmmievent">IESOpenMmiEvent</a>