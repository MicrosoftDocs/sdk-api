---
UID: NF:tuner.IESFileExpiryDateEvent.DoesExpireAfterFirstUse
title: IESFileExpiryDateEvent::DoesExpireAfterFirstUse (tuner.h)
description: Gets a flag from a FileExpiryDate event that indicates whether a license for protected content expires after its first use.
helpviewer_keywords: ["DoesExpireAfterFirstUse","DoesExpireAfterFirstUse method [Microsoft TV Technologies]","DoesExpireAfterFirstUse method [Microsoft TV Technologies]","IESFileExpiryDateEvent interface","IESFileExpiryDateEvent interface [Microsoft TV Technologies]","DoesExpireAfterFirstUse method","IESFileExpiryDateEvent.DoesExpireAfterFirstUse","IESFileExpiryDateEvent::DoesExpireAfterFirstUse","mstv.iesfileexpirydateevent_doesexpireafterfirstuse","tuner/IESFileExpiryDateEvent::DoesExpireAfterFirstUse"]
old-location: mstv\iesfileexpirydateevent_doesexpireafterfirstuse.htm
tech.root: mstv
ms.assetid: 24a1d5aa-fee5-4436-a3ee-6a2108ff0f32
ms.date: 12/05/2018
ms.keywords: DoesExpireAfterFirstUse, DoesExpireAfterFirstUse method [Microsoft TV Technologies], DoesExpireAfterFirstUse method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, IESFileExpiryDateEvent interface [Microsoft TV Technologies],DoesExpireAfterFirstUse method, IESFileExpiryDateEvent.DoesExpireAfterFirstUse, IESFileExpiryDateEvent::DoesExpireAfterFirstUse, mstv.iesfileexpirydateevent_doesexpireafterfirstuse, tuner/IESFileExpiryDateEvent::DoesExpireAfterFirstUse
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
 - IESFileExpiryDateEvent::DoesExpireAfterFirstUse
 - tuner/IESFileExpiryDateEvent::DoesExpireAfterFirstUse
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
 - IESFileExpiryDateEvent.DoesExpireAfterFirstUse
---

# IESFileExpiryDateEvent::DoesExpireAfterFirstUse


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a flag from a <b>FileExpiryDate</b> event that indicates whether a license for protected content expires after its first use.

## -parameters

### -param pfExpireAfterFirstUse [out, retval]

Receives the flag, which is true if the license expires after first use or false otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesfileexpirydateevent">IESFileExpiryDateEvent</a>