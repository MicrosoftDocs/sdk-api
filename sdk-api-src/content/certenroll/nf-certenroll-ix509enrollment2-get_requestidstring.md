---
UID: NF:certenroll.IX509Enrollment2.get_RequestIdString
title: IX509Enrollment2::get_RequestIdString
author: windows-sdk-content
description: Retrieves a string that contains a unique identifier for the certificate request sent to the certification enrollment server (CES).
old-location: security\ix509enrollment2_requestidstring.htm
old-project: seccertenroll
ms.assetid: a1269b0d-6b55-47ba-bca8-610c1032ecc4
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IX509Enrollment2 interface [Security],RequestIdString property, IX509Enrollment2.RequestIdString, IX509Enrollment2.get_RequestIdString, IX509Enrollment2::RequestIdString, IX509Enrollment2::get_RequestIdString, RequestIdString property [Security], RequestIdString property [Security],IX509Enrollment2 interface, certenroll/IX509Enrollment2::RequestIdString, certenroll/IX509Enrollment2::get_RequestIdString, get_RequestIdString, security.ix509enrollment2_requestidstring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Certenroll.h
api_name:
 - IX509Enrollment2.RequestIdString
 - IX509Enrollment2.get_RequestIdString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509Enrollment2::get_RequestIdString


## -description


The <b>RequestIdString</b> property retrieves a string that contains a unique identifier for the certificate request sent to the certification enrollment server (CES).

This property is read-only.


## -parameters


## -remarks



The value of the <b>RequestIdString</b> property is set during the enrollment process. It can be used during subsequent communication between the client and the CES. For example, if a CES marks a request as pending when initially submitted, the client can use the request ID string when it again contacts the CES and attempts to retrieve the certificate response.




## -see-also




<a href="https://msdn.microsoft.com/8e262b4b-de6a-417e-9ade-0b451bd4c09a">IX509Enrollment2</a>
 

 

