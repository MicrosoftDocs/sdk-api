---
UID: NF:tuner.IESFileExpiryDateEvent.IsEntitlementTokenPresent
title: IESFileExpiryDateEvent::IsEntitlementTokenPresent (tuner.h)
description: Gets a flag from FileExpiryDate event that indicates whether a license for protected content contains an entitlement token.
old-location: mstv\iesfileexpirydateevent_isentitlementtokenpresent.htm
tech.root: mstv
ms.assetid: 129c6df8-48d2-4e07-9e4e-82f13c4a3788
ms.date: 12/05/2018
ms.keywords: IESFileExpiryDateEvent interface [Microsoft TV Technologies],IsEntitlementTokenPresent method, IESFileExpiryDateEvent.IsEntitlementTokenPresent, IESFileExpiryDateEvent::IsEntitlementTokenPresent, IsEntitlementTokenPresent, IsEntitlementTokenPresent method [Microsoft TV Technologies], IsEntitlementTokenPresent method [Microsoft TV Technologies],IESFileExpiryDateEvent interface, mstv.iesfileexpirydateevent_isentitlementtokenpresent, tuner/IESFileExpiryDateEvent::IsEntitlementTokenPresent
f1_keywords:
- tuner/IESFileExpiryDateEvent.IsEntitlementTokenPresent
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
- IESFileExpiryDateEvent.IsEntitlementTokenPresent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesfileexpirydateevent">IESFileExpiryDateEvent</a>
 

 

