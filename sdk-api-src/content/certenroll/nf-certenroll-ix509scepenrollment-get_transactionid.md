---
UID: NF:certenroll.IX509SCEPEnrollment.get_TransactionId
title: IX509SCEPEnrollment::get_TransactionId (certenroll.h)
author: windows-sdk-content
description: Gets or sets the transaction id for the request.
old-location: security\ix509scepenrollment_transactionid.htm
tech.root: seccertenroll
ms.assetid: f0688ce9-9c20-4726-ae15-69285c3b30f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509SCEPEnrollment interface [Security],TransactionId property, IX509SCEPEnrollment.TransactionId, IX509SCEPEnrollment.get_TransactionId, IX509SCEPEnrollment::TransactionId, IX509SCEPEnrollment::get_TransactionId, IX509SCEPEnrollment::put_TransactionId, TransactionId property [Security], TransactionId property [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::TransactionId, certenroll/IX509SCEPEnrollment::get_TransactionId, certenroll/IX509SCEPEnrollment::put_TransactionId, get_TransactionId, security.ix509scepenrollment_transactionid
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
 - IX509SCEPEnrollment.TransactionId
 - IX509SCEPEnrollment.get_TransactionId
 - IX509SCEPEnrollment.put_TransactionId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509SCEPEnrollment::get_TransactionId


## -description


Gets or sets the transaction id for the request.

This property is read/write.


## -parameters


## -remarks



If you do not specify a transaction id, then the <a href="https://msdn.microsoft.com/b86d6dc3-aa96-45f3-9551-f24c39ea6cbf">CreateRequestMessage</a> method will create one. If the transaction id has not been set or the <b>CreateRequestMessage</b>  method has not been called, then this property will return <b>CERTSRV_E_PROPERTY_EMPTY</b>.

After processing a pending request, the caller must save this value for later use when calling the <a href="https://msdn.microsoft.com/86d031b0-2009-460b-8bed-fe7a0489f22b">CreateRetrievePendingMessage</a> method to format a message to be sent to the SCEP server to poll for the issued certificate.

Set this property before you call the <a href="https://msdn.microsoft.com/4254fdf3-473f-4f22-a08f-13481fd9f779">ProcessResponseMessage</a> method when you are using a new instance of the <a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a> interface to install the response.

Set this property before you call the <a href="https://msdn.microsoft.com/86d031b0-2009-460b-8bed-fe7a0489f22b">CreateRetrievePendingMessage</a> method when you are using a new instance of the <a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a> interface to create a retrieval message.




## -see-also




<a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a>
 

 

