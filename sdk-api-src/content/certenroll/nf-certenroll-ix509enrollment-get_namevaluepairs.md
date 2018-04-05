---
UID: NF:certenroll.IX509Enrollment.get_NameValuePairs
title: IX509Enrollment::get_NameValuePairs method
author: windows-driver-content
description: Retrieves a collection of name-value pairs associated with the enrollment object.
old-location: security\ix509enrollment_namevaluepairs_property.htm
old-project: SecCertEnroll
ms.assetid: d682fb7c-de80-4285-baa2-f86c997f0987
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IX509Enrollment, IX509Enrollment interface [Security], NameValuePairs property, IX509Enrollment.NameValuePairs, IX509Enrollment::get_NameValuePairs, NameValuePairs property [Security], NameValuePairs property [Security], IX509Enrollment interface, certenroll/IX509Enrollment::NameValuePairs, certenroll/IX509Enrollment::get_NameValuePairs, get_NameValuePairs,IX509Enrollment.get_NameValuePairs, security.ix509enrollment_namevaluepairs_property
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509Enrollment.NameValuePairs
-	IX509Enrollment.get_NameValuePairs
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509Enrollment::get_NameValuePairs method


## -description


The <b>NameValuePairs</b> property retrieves a collection of name-value pairs associated with the enrollment object.

This property is read-only.


## -parameters


## -remarks



name-value pairs are passed to the certification authority (CA) with the request for the CA to act upon. The <a href="https://msdn.microsoft.com/c881dc9f-4187-4ba1-9f3a-e1564e4f37c7">IX509NameValuePairs</a> object is associated with the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> object when the object is initialized. Therefore, before calling this property, you must initialize the <b>IX509Enrollment</b> object by calling one of the following methods.<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/04cb00af-f786-4548-bee3-2cc5083278c3">InitializeFromRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/44a934f4-9ae9-4f52-9d44-f5fcf30f3837">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
 

 

