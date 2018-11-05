---
UID: NF:certenroll.IX509SCEPEnrollment.get_TransactionId
title: IX509SCEPEnrollment::get_TransactionId
author: windows-sdk-content
description: Gets or sets the transaction id for the request.
old-location: security\ix509scepenrollment_transactionid.htm
tech.root: SecCertEnroll
ms.assetid: f0688ce9-9c20-4726-ae15-69285c3b30f3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509SCEPEnrollment interface [Security],TransactionId property, IX509SCEPEnrollment.TransactionId, IX509SCEPEnrollment.get_TransactionId, IX509SCEPEnrollment::TransactionId, IX509SCEPEnrollment::get_TransactionId, IX509SCEPEnrollment::put_TransactionId, TransactionId property [Security], TransactionId property [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::TransactionId, certenroll/IX509SCEPEnrollment::get_TransactionId, certenroll/IX509SCEPEnrollment::put_TransactionId, get_TransactionId, security.ix509scepenrollment_transactionid
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



If you do not specify a transaction id, then the <a href="https://msdn.microsoft.com/en-us/library/Dn424976(v=VS.85).aspx">CreateRequestMessage</a> method will create one. If the transaction id has not been set or the <b>CreateRequestMessage</b>  method has not been called, then this property will return <b>CERTSRV_E_PROPERTY_EMPTY</b>.

After processing a pending request, the caller must save this value for later use when calling the <a href="https://msdn.microsoft.com/en-us/library/Dn424978(v=VS.85).aspx">CreateRetrievePendingMessage</a> method to format a message to be sent to the SCEP server to poll for the issued certificate.

Set this property before you call the <a href="https://msdn.microsoft.com/en-us/library/Dn424985(v=VS.85).aspx">ProcessResponseMessage</a> method when you are using a new instance of the <a href="https://msdn.microsoft.com/en-us/library/Dn424973(v=VS.85).aspx">IX509SCEPEnrollment</a> interface to install the response.

Set this property before you call the <a href="https://msdn.microsoft.com/en-us/library/Dn424978(v=VS.85).aspx">CreateRetrievePendingMessage</a> method when you are using a new instance of the <a href="https://msdn.microsoft.com/en-us/library/Dn424973(v=VS.85).aspx">IX509SCEPEnrollment</a> interface to create a retrieval message.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn424973(v=VS.85).aspx">IX509SCEPEnrollment</a>
 

 

