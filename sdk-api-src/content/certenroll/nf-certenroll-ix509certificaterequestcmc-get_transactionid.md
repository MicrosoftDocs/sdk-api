---
UID: NF:certenroll.IX509CertificateRequestCmc.get_TransactionId
title: IX509CertificateRequestCmc::get_TransactionId
author: windows-sdk-content
description: Specifies or retrieves a transaction identifier that can be used to track a certificate request or response.
old-location: security\ix509certificaterequestcmc_transactionid_property.htm
tech.root: seccertenroll
ms.assetid: 0d47e4b6-47bb-4ec4-8248-f4c859e9b9da
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],TransactionId property, IX509CertificateRequestCmc.TransactionId, IX509CertificateRequestCmc.get_TransactionId, IX509CertificateRequestCmc::TransactionId, IX509CertificateRequestCmc::get_TransactionId, IX509CertificateRequestCmc::put_TransactionId, TransactionId property [Security], TransactionId property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::TransactionId, certenroll/IX509CertificateRequestCmc::get_TransactionId, certenroll/IX509CertificateRequestCmc::put_TransactionId, get_TransactionId, security.ix509certificaterequestcmc_transactionid_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequestCmc.TransactionId
 - IX509CertificateRequestCmc.get_TransactionId
 - IX509CertificateRequestCmc.put_TransactionId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestCmc::get_TransactionId


## -description


The <b>TransactionId</b> property specifies or retrieves a transaction identifier that can be used to track a certificate request or response.

This property is read/write.


## -parameters


## -remarks



 A round trip certificate request and response transaction can be tracked using an identifier.  The client generates a transaction ID and
   retains it until the certificate or registration authority responds with a message that
   completes the transaction.  The  response includes the identifier.

You must set this property, if at all,  before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method, but you must initialize the CMC request object before calling the property. For more information, see the following topics:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377669(v=VS.85).aspx">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377610(v=VS.85).aspx">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377613(v=VS.85).aspx">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377616(v=VS.85).aspx">InitializeFromInnerRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377257(v=VS.85).aspx">InitializeFromInnerRequestTemplateName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377622(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>
 

 

