---
UID: NF:certenroll.ICspAlgorithm.get_Valid
title: ICspAlgorithm::get_Valid (certenroll.h)
author: windows-sdk-content
description: Retrieves a Boolean value that specifies whether the algorithm object is valid.
old-location: security\icspalgorithm_valid_property.htm
tech.root: seccertenroll
ms.assetid: 8f8e9f23-f857-49d3-9519-061ccce27514
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICspAlgorithm interface [Security],Valid property, ICspAlgorithm.Valid, ICspAlgorithm.get_Valid, ICspAlgorithm::Valid, ICspAlgorithm::get_Valid, Valid property [Security], Valid property [Security],ICspAlgorithm interface, certenroll/ICspAlgorithm::Valid, certenroll/ICspAlgorithm::get_Valid, get_Valid, security.icspalgorithm_valid_property
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
 - ICspAlgorithm.Valid
 - ICspAlgorithm.get_Valid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspAlgorithm::get_Valid


## -description


The <b>Valid</b> property retrieves a Boolean value that specifies whether the algorithm object is valid.

This property is read-only.


## -parameters


## -remarks



If a template refers to an algorithm that is not supported by the specified cryptographic provider, the enrollment process creates a placeholder <a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a> object, sets the <b>Valid</b> property to false, and sets the <a href="https://msdn.microsoft.com/af7fa894-58e2-4607-9b6e-c32d4f412ddf">Name</a> property. No other property values are defined.

You must call the <a href="https://msdn.microsoft.com/b405503f-2af5-4a2f-abdb-e2eb108c4b1b">InitializeFromName</a> method or the <a href="https://msdn.microsoft.com/24466981-2ea2-41f5-b2db-85b5629fba7d">InitializeFromType</a> method on the <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> interface before calling this property.

<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) is defined by the X.680 through X.683 standards. The Certificate Enrollment API verifies an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) by <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoding it and then decoding the result to make certain that the OID remains unchanged and by checking that the following are true:<ul>
<li>The first number in the OID is either 0, 1, or 2.</li>
<li>All other characters are either digits (0 to 9) or periods (.).</li>
<li>No periods start or end the OID.</li>
<li>No consecutive characters are both periods.</li>
<li>The OID must contain at least one period.</li>
<li>If the first number is 0 or 1, the second number must be between 0 and 39 inclusive.</li>
<li>If the first number is 2, the second number can be any value.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a>
 

 

