---
UID: NF:tuner.IESFileExpiryDateEvent.GetFinalExpiryDate
title: IESFileExpiryDateEvent::GetFinalExpiryDate method
author: windows-driver-content
description: Gets the date from a FileExpiryDate event that indicates when a renewable license for protected content finally expires.
old-location: mstv\iesfileexpirydateevent_getfinalexpirydate.htm
old-project: mstv
ms.assetid: 903ecf69-8da1-47a4-acce-50d37565e480
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetFinalExpiryDate method [Microsoft TV Technologies], GetFinalExpiryDate method [Microsoft TV Technologies], IESFileExpiryDateEvent interface, GetFinalExpiryDate,IESFileExpiryDateEvent.GetFinalExpiryDate, IESFileExpiryDateEvent, IESFileExpiryDateEvent interface [Microsoft TV Technologies], GetFinalExpiryDate method, IESFileExpiryDateEvent::GetFinalExpiryDate, mstv.iesfileexpirydateevent_getfinalexpirydate, tuner/IESFileExpiryDateEvent::GetFinalExpiryDate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESFileExpiryDateEvent.GetFinalExpiryDate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESFileExpiryDateEvent::GetFinalExpiryDate method


## -description


Gets the date from a  <b>FileExpiryDate</b> event that indicates when a renewable license for protected content finally expires. 


## -parameters




### -param pqwExpiryDate [out, retval]

Receives the final expiry date.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6c89a3ee-7d69-4cde-b1e5-b566fa1c2ca3">IESFileExpiryDateEvent</a>
 

 

