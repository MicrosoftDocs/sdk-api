---
UID: NF:tuner.IESFileExpiryDateEvent.GetExpiryDate
title: IESFileExpiryDateEvent::GetExpiryDate (tuner.h)
author: windows-sdk-content
description: Gets the date from a FileExpiryDate event that indicates when a license for protected content expires.
old-location: mstv\iesfileexpirydateevent_getexpirydate.htm
tech.root: mstv
ms.assetid: 1d89c613-002b-4c90-832f-32bc268752a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetExpiryDate, GetExpiryDate method [Microsoft TV Technologies], GetExpiryDate method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, IESFileExpiryDateEvent interface [Microsoft TV Technologies],GetExpiryDate method, IESFileExpiryDateEvent.GetExpiryDate, IESFileExpiryDateEvent::GetExpiryDate, mstv.iesfileexpirydateevent_getexpirydate, tuner/IESFileExpiryDateEvent::GetExpiryDate
ms.topic: method
f1_keywords: 
 - "tuner/IESFileExpiryDateEvent.GetExpiryDate"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESFileExpiryDateEvent.GetExpiryDate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESFileExpiryDateEvent::GetExpiryDate


## -description


Gets the date from a <b>FileExpiryDate</b> event that indicates when a license for protected content expires.


## -parameters




### -param pqwExpiryDate [out, retval]

Receives the expiry date from the event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesfileexpirydateevent">IESFileExpiryDateEvent</a>
 

 

