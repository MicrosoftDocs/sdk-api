---
UID: NF:tuner.IESFileExpiryDateEvent.GetMaxRenewalCount
title: IESFileExpiryDateEvent::GetMaxRenewalCount
author: windows-sdk-content
description: Gets the maximum number of times that a license for protected content can be renewed from a FileExpiryDate event.
old-location: mstv\iesfileexpirydateevent_getmaxrenewalcount.htm
old-project: mstv
ms.assetid: 3e823f7f-91cc-4e59-bbb5-1a33ef094999
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetMaxRenewalCount, GetMaxRenewalCount method [Microsoft TV Technologies], GetMaxRenewalCount method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, IESFileExpiryDateEvent interface [Microsoft TV Technologies],GetMaxRenewalCount method, IESFileExpiryDateEvent.GetMaxRenewalCount, IESFileExpiryDateEvent::GetMaxRenewalCount, mstv.iesfileexpirydateevent_getmaxrenewalcount, tuner/IESFileExpiryDateEvent::GetMaxRenewalCount
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESFileExpiryDateEvent.GetMaxRenewalCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESFileExpiryDateEvent::GetMaxRenewalCount


## -description


Gets the maximum number of times that a license for protected content can be renewed from a <b>FileExpiryDate</b> event.


## -parameters




### -param dwMaxRenewalCount [out, retval]

Receives the maximum renewal count.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6c89a3ee-7d69-4cde-b1e5-b566fa1c2ca3">IESFileExpiryDateEvent</a>
 

 

