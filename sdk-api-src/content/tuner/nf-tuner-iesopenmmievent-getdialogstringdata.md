---
UID: NF:tuner.IESOpenMmiEvent.GetDialogStringData
title: IESOpenMmiEvent::GetDialogStringData (tuner.h)
description: Gets the data associated with an OpenMMI event, in Unicode string format. This data can be the contents of the dialog that is opened or the Uniform Resource Locator (URL) that contains the dialog.
helpviewer_keywords: ["GetDialogStringData","GetDialogStringData method [Microsoft TV Technologies]","GetDialogStringData method [Microsoft TV Technologies]","IESOpenMmiEvent interface","IESOpenMmiEvent interface [Microsoft TV Technologies]","GetDialogStringData method","IESOpenMmiEvent.GetDialogStringData","IESOpenMmiEvent::GetDialogStringData","mstv.iesopenmmievent_getdialogstringdata","tuner/IESOpenMmiEvent::GetDialogStringData"]
old-location: mstv\iesopenmmievent_getdialogstringdata.htm
tech.root: mstv
ms.assetid: 5652ff59-e0ce-4acd-b62a-807d7a307e5b
ms.date: 12/05/2018
ms.keywords: GetDialogStringData, GetDialogStringData method [Microsoft TV Technologies], GetDialogStringData method [Microsoft TV Technologies],IESOpenMmiEvent interface, IESOpenMmiEvent interface [Microsoft TV Technologies],GetDialogStringData method, IESOpenMmiEvent.GetDialogStringData, IESOpenMmiEvent::GetDialogStringData, mstv.iesopenmmievent_getdialogstringdata, tuner/IESOpenMmiEvent::GetDialogStringData
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
 - IESOpenMmiEvent::GetDialogStringData
 - tuner/IESOpenMmiEvent::GetDialogStringData
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
 - IESOpenMmiEvent.GetDialogStringData
---

# IESOpenMmiEvent::GetDialogStringData


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the data associated with an <b>OpenMMI </b> event, in Unicode string format. This data can be the contents of the dialog that is opened or the Uniform Resource Locator (URL) that contains the dialog.

## -parameters

### -param pbstrBaseUrl [out]

Pointer to a string that receives the URL containing the dialog.
          The caller is responsible for freeing this memory.

### -param pbstrData [out, retval]

Pointer to the string that receives the dialog contents.
          The caller is responsible for freeing the memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesopenmmievent">IESOpenMmiEvent</a>