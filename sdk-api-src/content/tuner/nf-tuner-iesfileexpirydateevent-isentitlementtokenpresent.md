---
UID: NF:tuner.IESFileExpiryDateEvent.IsEntitlementTokenPresent
title: IESFileExpiryDateEvent::IsEntitlementTokenPresent
author: windows-sdk-content
description: Gets a flag from FileExpiryDate event that indicates whether a license for protected content contains an entitlement token.
old-location: mstv\iesfileexpirydateevent_isentitlementtokenpresent.htm
old-project: mstv
ms.assetid: 129c6df8-48d2-4e07-9e4e-82f13c4a3788
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IESFileExpiryDateEvent interface [Microsoft TV Technologies],IsEntitlementTokenPresent method, IESFileExpiryDateEvent.IsEntitlementTokenPresent, IESFileExpiryDateEvent::IsEntitlementTokenPresent, IsEntitlementTokenPresent, IsEntitlementTokenPresent method [Microsoft TV Technologies], IsEntitlementTokenPresent method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, mstv.iesfileexpirydateevent_isentitlementtokenpresent, tuner/IESFileExpiryDateEvent::IsEntitlementTokenPresent
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
 - IESFileExpiryDateEvent.IsEntitlementTokenPresent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESFileExpiryDateEvent::IsEntitlementTokenPresent


## -description


Gets a flag from <b>FileExpiryDate</b> event that indicates whether a license for protected content contains an entitlement token. Media transform devices  and media sink devices  in a Protected Broadcast Driver Architecture (PBDA) filter graph can use entitlement tokens to verify whether users can access protected content.


## -parameters




### -param pfEntTokenPresent [out, retval]

Receives the flag, which is true if the license for protected content contains an entitlement token or false otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6c89a3ee-7d69-4cde-b1e5-b566fa1c2ca3">IESFileExpiryDateEvent</a>
 

 

