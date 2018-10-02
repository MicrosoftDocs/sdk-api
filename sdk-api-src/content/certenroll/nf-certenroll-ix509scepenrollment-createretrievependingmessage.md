---
UID: NF:certenroll.IX509SCEPEnrollment.CreateRetrievePendingMessage
title: IX509SCEPEnrollment::CreateRetrievePendingMessage
author: windows-sdk-content
description: Create a message for certificate polling (manual enrollment).
old-location: security\ix509scepenrollment_createretrievependingmessage.htm
tech.root: SecCertEnroll
ms.assetid: 86d031b0-2009-460b-8bed-fe7a0489f22b
ms.author: windowssdkdev
ms.date: 09/26/2018
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



You must call the <a href="https://msdn.microsoft.com/en-us/library/Dn424982(v=VS.85).aspx">InitializeForPending</a> method before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn424973(v=VS.85).aspx">IX509SCEPEnrollment</a>
 

 

