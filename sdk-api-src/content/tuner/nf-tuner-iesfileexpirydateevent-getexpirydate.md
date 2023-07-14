---
UID: NF:tuner.IESFileExpiryDateEvent.GetExpiryDate
title: IESFileExpiryDateEvent::GetExpiryDate (tuner.h)
description: Gets the date from a FileExpiryDate event that indicates when a license for protected content expires.
helpviewer_keywords: ["GetExpiryDate","GetExpiryDate method [Microsoft TV Technologies]","GetExpiryDate method [Microsoft TV Technologies]","IESFileExpiryDateEvent interface","IESFileExpiryDateEvent interface [Microsoft TV Technologies]","GetExpiryDate method","IESFileExpiryDateEvent.GetExpiryDate","IESFileExpiryDateEvent::GetExpiryDate","mstv.iesfileexpirydateevent_getexpirydate","tuner/IESFileExpiryDateEvent::GetExpiryDate"]
old-location: mstv\iesfileexpirydateevent_getexpirydate.htm
tech.root: mstv
ms.assetid: 1d89c613-002b-4c90-832f-32bc268752a4
ms.date: 12/05/2018
ms.keywords: GetExpiryDate, GetExpiryDate method [Microsoft TV Technologies], GetExpiryDate method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, IESFileExpiryDateEvent interface [Microsoft TV Technologies],GetExpiryDate method, IESFileExpiryDateEvent.GetExpiryDate, IESFileExpiryDateEvent::GetExpiryDate, mstv.iesfileexpirydateevent_getexpirydate, tuner/IESFileExpiryDateEvent::GetExpiryDate
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
 - IESFileExpiryDateEvent::GetExpiryDate
 - tuner/IESFileExpiryDateEvent::GetExpiryDate
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
 - IESFileExpiryDateEvent.GetExpiryDate
---

# IESFileExpiryDateEvent::GetExpiryDate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the date from a <b>FileExpiryDate</b> event that indicates when a license for protected content expires.

## -parameters

### -param pqwExpiryDate [out, retval]

Receives the expiry date from the event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesfileexpirydateevent">IESFileExpiryDateEvent</a>