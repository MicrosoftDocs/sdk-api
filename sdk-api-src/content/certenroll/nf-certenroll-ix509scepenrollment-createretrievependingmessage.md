---
UID: NF:certenroll.IX509SCEPEnrollment.CreateRetrievePendingMessage
title: IX509SCEPEnrollment::CreateRetrievePendingMessage
author: windows-sdk-content
description: Create a message for certificate polling (manual enrollment).
old-location: security\ix509scepenrollment_createretrievependingmessage.htm
tech.root: seccertenroll
ms.assetid: 86d031b0-2009-460b-8bed-fe7a0489f22b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateRetrievePendingMessage, CreateRetrievePendingMessage method [Security], CreateRetrievePendingMessage method [Security],IX509SCEPEnrollment interface, IX509SCEPEnrollment interface [Security],CreateRetrievePendingMessage method, IX509SCEPEnrollment.CreateRetrievePendingMessage, IX509SCEPEnrollment::CreateRetrievePendingMessage, certenroll/IX509SCEPEnrollment::CreateRetrievePendingMessage, security.ix509scepenrollment_createretrievependingmessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509SCEPEnrollment.CreateRetrievePendingMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509SCEPEnrollment::CreateRetrievePendingMessage


## -description


Create a message for certificate polling (manual enrollment).


## -parameters




### -param Encoding [in]


### -param pValue [out, retval]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must call the <a href="https://msdn.microsoft.com/6b6f9e9d-5316-4928-861a-22497e1f5c00">InitializeForPending</a> method before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a>
 

 

