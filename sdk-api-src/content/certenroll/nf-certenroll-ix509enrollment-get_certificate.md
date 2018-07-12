---
UID: NF:certenroll.IX509Enrollment.get_Certificate
title: IX509Enrollment::get_Certificate
author: windows-sdk-content
description: Retrieves the installed certificate.
old-location: security\ix509enrollment_certificate_property.htm
old-project: seccertenroll
ms.assetid: 636e4c6d-38b9-4a27-b640-4c071816ee97
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: Certificate property [Security], Certificate property [Security],IX509Enrollment interface, IX509Enrollment interface [Security],Certificate property, IX509Enrollment.Certificate, IX509Enrollment.get_Certificate, IX509Enrollment::Certificate, IX509Enrollment::get_Certificate, certenroll/IX509Enrollment::Certificate, certenroll/IX509Enrollment::get_Certificate, get_Certificate, security.ix509enrollment_certificate_property
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509Enrollment.Certificate
 - IX509Enrollment.get_Certificate
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509Enrollment::get_Certificate


## -description


The <b>Certificate</b> property retrieves the installed certificate. The certificate is contained in a byte array that is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard.  The DER-encoded byte array is represented by a string that is  either a pure binary sequence or Unicode encoded.

This property is read-only.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
 

 

