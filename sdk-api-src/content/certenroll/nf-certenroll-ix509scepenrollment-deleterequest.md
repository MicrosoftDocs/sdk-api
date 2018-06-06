---
UID: NF:certenroll.IX509SCEPEnrollment.DeleteRequest
title: IX509SCEPEnrollment::DeleteRequest
author: windows-sdk-content
description: Delete any certificates or keys created for the request.
old-location: security\ix509scepenrollment_deleterequest.htm
old-project: SecCertEnroll
ms.assetid: d709dd46-b6ed-4471-a601-e140a139f57e
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: DeleteRequest, DeleteRequest method [Security], DeleteRequest method [Security],IX509SCEPEnrollment interface, IX509SCEPEnrollment interface [Security],DeleteRequest method, IX509SCEPEnrollment.DeleteRequest, IX509SCEPEnrollment::DeleteRequest, certenroll/IX509SCEPEnrollment::DeleteRequest, security.ix509scepenrollment_deleterequest
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509SCEPEnrollment.DeleteRequest
product: Windows
targetos: Windows
req.lib: 
req.dll: Certenroll.dll
req.irql: 
---

# IX509SCEPEnrollment::DeleteRequest


## -description


Delete any certificates or keys created for the request.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must set the <a href="https://msdn.microsoft.com/f0688ce9-9c20-4726-ae15-69285c3b30f3">TransactionId</a> property and call the <a href="https://msdn.microsoft.com/6b6f9e9d-5316-4928-861a-22497e1f5c00">InitializeForPending</a> method before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a>
 

 

