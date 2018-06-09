---
UID: NF:tuner.IESFileExpiryDateEvent.DoesExpireAfterFirstUse
title: IESFileExpiryDateEvent::DoesExpireAfterFirstUse
author: windows-sdk-content
description: Gets a flag from a FileExpiryDate event that indicates whether a license for protected content expires after its first use.
old-location: mstv\iesfileexpirydateevent_doesexpireafterfirstuse.htm
old-project: mstv
ms.assetid: 24a1d5aa-fee5-4436-a3ee-6a2108ff0f32
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: DoesExpireAfterFirstUse, DoesExpireAfterFirstUse method [Microsoft TV Technologies], DoesExpireAfterFirstUse method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, IESFileExpiryDateEvent interface [Microsoft TV Technologies],DoesExpireAfterFirstUse method, IESFileExpiryDateEvent.DoesExpireAfterFirstUse, IESFileExpiryDateEvent::DoesExpireAfterFirstUse, mstv.iesfileexpirydateevent_doesexpireafterfirstuse, tuner/IESFileExpiryDateEvent::DoesExpireAfterFirstUse
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
 - IESFileExpiryDateEvent.DoesExpireAfterFirstUse
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESFileExpiryDateEvent::DoesExpireAfterFirstUse


## -description


Gets a flag from a <b>FileExpiryDate</b> event that indicates whether a license for protected content expires after its first use.


## -parameters




### -param pfExpireAfterFirstUse [out, retval]

Receives the flag, which is true if the license expires after first use or false otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6c89a3ee-7d69-4cde-b1e5-b566fa1c2ca3">IESFileExpiryDateEvent</a>
 

 

