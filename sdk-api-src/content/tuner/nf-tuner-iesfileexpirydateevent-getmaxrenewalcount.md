---
UID: NF:tuner.IESFileExpiryDateEvent.GetMaxRenewalCount
title: IESFileExpiryDateEvent::GetMaxRenewalCount (tuner.h)
description: Gets the maximum number of times that a license for protected content can be renewed from a FileExpiryDate event.
helpviewer_keywords: ["GetMaxRenewalCount","GetMaxRenewalCount method [Microsoft TV Technologies]","GetMaxRenewalCount method [Microsoft TV Technologies]","IESFileExpiryDateEvent interface","IESFileExpiryDateEvent interface [Microsoft TV Technologies]","GetMaxRenewalCount method","IESFileExpiryDateEvent.GetMaxRenewalCount","IESFileExpiryDateEvent::GetMaxRenewalCount","mstv.iesfileexpirydateevent_getmaxrenewalcount","tuner/IESFileExpiryDateEvent::GetMaxRenewalCount"]
old-location: mstv\iesfileexpirydateevent_getmaxrenewalcount.htm
tech.root: mstv
ms.assetid: 3e823f7f-91cc-4e59-bbb5-1a33ef094999
ms.date: 12/05/2018
ms.keywords: GetMaxRenewalCount, GetMaxRenewalCount method [Microsoft TV Technologies], GetMaxRenewalCount method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, IESFileExpiryDateEvent interface [Microsoft TV Technologies],GetMaxRenewalCount method, IESFileExpiryDateEvent.GetMaxRenewalCount, IESFileExpiryDateEvent::GetMaxRenewalCount, mstv.iesfileexpirydateevent_getmaxrenewalcount, tuner/IESFileExpiryDateEvent::GetMaxRenewalCount
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
 - IESFileExpiryDateEvent::GetMaxRenewalCount
 - tuner/IESFileExpiryDateEvent::GetMaxRenewalCount
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
 - IESFileExpiryDateEvent.GetMaxRenewalCount
---

# IESFileExpiryDateEvent::GetMaxRenewalCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the maximum number of times that a license for protected content can be renewed from a <b>FileExpiryDate</b> event.

## -parameters

### -param dwMaxRenewalCount [out, retval]

Receives the maximum renewal count.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesfileexpirydateevent">IESFileExpiryDateEvent</a>