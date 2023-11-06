---
UID: NF:tuner.IESFileExpiryDateEvent.GetFinalExpiryDate
title: IESFileExpiryDateEvent::GetFinalExpiryDate (tuner.h)
description: Gets the date from a FileExpiryDate event that indicates when a renewable license for protected content finally expires.
helpviewer_keywords: ["GetFinalExpiryDate","GetFinalExpiryDate method [Microsoft TV Technologies]","GetFinalExpiryDate method [Microsoft TV Technologies]","IESFileExpiryDateEvent interface","IESFileExpiryDateEvent interface [Microsoft TV Technologies]","GetFinalExpiryDate method","IESFileExpiryDateEvent.GetFinalExpiryDate","IESFileExpiryDateEvent::GetFinalExpiryDate","mstv.iesfileexpirydateevent_getfinalexpirydate","tuner/IESFileExpiryDateEvent::GetFinalExpiryDate"]
old-location: mstv\iesfileexpirydateevent_getfinalexpirydate.htm
tech.root: mstv
ms.assetid: 903ecf69-8da1-47a4-acce-50d37565e480
ms.date: 12/05/2018
ms.keywords: GetFinalExpiryDate, GetFinalExpiryDate method [Microsoft TV Technologies], GetFinalExpiryDate method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, IESFileExpiryDateEvent interface [Microsoft TV Technologies],GetFinalExpiryDate method, IESFileExpiryDateEvent.GetFinalExpiryDate, IESFileExpiryDateEvent::GetFinalExpiryDate, mstv.iesfileexpirydateevent_getfinalexpirydate, tuner/IESFileExpiryDateEvent::GetFinalExpiryDate
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
 - IESFileExpiryDateEvent::GetFinalExpiryDate
 - tuner/IESFileExpiryDateEvent::GetFinalExpiryDate
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
 - IESFileExpiryDateEvent.GetFinalExpiryDate
---

# IESFileExpiryDateEvent::GetFinalExpiryDate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the date from a  <b>FileExpiryDate</b> event that indicates when a renewable license for protected content finally expires.

## -parameters

### -param pqwExpiryDate [out, retval]

Receives the final expiry date.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesfileexpirydateevent">IESFileExpiryDateEvent</a>