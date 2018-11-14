---
UID: NF:tuner.IESFileExpiryDateEvent.GetFinalExpiryDate
title: IESFileExpiryDateEvent::GetFinalExpiryDate
author: windows-sdk-content
description: Gets the date from a FileExpiryDate event that indicates when a renewable license for protected content finally expires.
old-location: mstv\iesfileexpirydateevent_getfinalexpirydate.htm
tech.root: MSTV
ms.assetid: 903ecf69-8da1-47a4-acce-50d37565e480
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetFinalExpiryDate, GetFinalExpiryDate method [Microsoft TV Technologies], GetFinalExpiryDate method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, IESFileExpiryDateEvent interface [Microsoft TV Technologies],GetFinalExpiryDate method, IESFileExpiryDateEvent.GetFinalExpiryDate, IESFileExpiryDateEvent::GetFinalExpiryDate, mstv.iesfileexpirydateevent_getfinalexpirydate, tuner/IESFileExpiryDateEvent::GetFinalExpiryDate
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
 - IESFileExpiryDateEvent.GetFinalExpiryDate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tuner.h
: 
- IESFileExpiryDateEvent.GetFinalExpiryDate
: 
---

# IESFileExpiryDateEvent::GetFinalExpiryDate


## -description


Gets the date from a  <b>FileExpiryDate</b> event that indicates when a renewable license for protected content finally expires. 


## -parameters




### -param pqwExpiryDate [out, retval]

Receives the final expiry date.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6c89a3ee-7d69-4cde-b1e5-b566fa1c2ca3">IESFileExpiryDateEvent</a>
 

 

