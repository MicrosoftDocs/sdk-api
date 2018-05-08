---
UID: NF:certenroll.IX509Enrollment.get_Response
title: IX509Enrollment::get_Response
author: windows-driver-content
description: Retrieves the certificate response returned from a certification authority.
old-location: security\ix509enrollment_response_property.htm
old-project: SecCertEnroll
ms.assetid: 4580d376-0dbb-4418-a542-b0a9710862c4
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509Enrollment interface [Security],Response property, IX509Enrollment.Response, IX509Enrollment.get_Response, IX509Enrollment::Response, IX509Enrollment::get_Response, Response property [Security], Response property [Security],IX509Enrollment interface, certenroll/IX509Enrollment::Response, certenroll/IX509Enrollment::get_Response, get_Response, security.ix509enrollment_response_property
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
-	IX509Enrollment.Response
-	IX509Enrollment.get_Response
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509Enrollment::get_Response


## -description


The <b>Response</b> property retrieves the certificate response returned from a certification authority. The response is contained in a byte array that is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard.  The DER-encoded byte array is represented by a string that is  either a pure binary sequence or Unicode encoded.

This property is read-only.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
 

 

