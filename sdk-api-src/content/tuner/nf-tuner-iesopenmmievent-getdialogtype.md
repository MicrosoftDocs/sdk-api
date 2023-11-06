---
UID: NF:tuner.IESOpenMmiEvent.GetDialogType
title: IESOpenMmiEvent::GetDialogType (tuner.h)
description: The GetDialogType method gets the GUID representing the experience type of the dialog that is being opened.
helpviewer_keywords: ["GetDialogType","GetDialogType method [Microsoft TV Technologies]","GetDialogType method [Microsoft TV Technologies]","IESOpenMmiEvent interface","IESOpenMmiEvent interface [Microsoft TV Technologies]","GetDialogType method","IESOpenMmiEvent.GetDialogType","IESOpenMmiEvent::GetDialogType","mstv.iesopenmmievent_getdialogtype","tuner/IESOpenMmiEvent::GetDialogType"]
old-location: mstv\iesopenmmievent_getdialogtype.htm
tech.root: mstv
ms.assetid: 93f3cd5e-7d8e-42b9-a688-3df22855e7fb
ms.date: 12/05/2018
ms.keywords: GetDialogType, GetDialogType method [Microsoft TV Technologies], GetDialogType method [Microsoft TV Technologies],IESOpenMmiEvent interface, IESOpenMmiEvent interface [Microsoft TV Technologies],GetDialogType method, IESOpenMmiEvent.GetDialogType, IESOpenMmiEvent::GetDialogType, mstv.iesopenmmievent_getdialogtype, tuner/IESOpenMmiEvent::GetDialogType
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
 - IESOpenMmiEvent::GetDialogType
 - tuner/IESOpenMmiEvent::GetDialogType
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
 - IESOpenMmiEvent.GetDialogType
---

# IESOpenMmiEvent::GetDialogType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetDialogType</b> method gets the GUID representing the experience type of the dialog that is being opened.

## -parameters

### -param guidDialogType [out, retval]

Gets the GUID identifying the experience type of the dialog. If the application does not recognize the experience type, it should set the event as complete  by returning an ERROR_ INVALID_TYPE result.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesopenmmievent">IESOpenMmiEvent</a>