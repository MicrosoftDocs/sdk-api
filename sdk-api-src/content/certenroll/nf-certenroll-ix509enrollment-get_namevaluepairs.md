---
UID: NF:certenroll.IX509Enrollment.get_NameValuePairs
title: IX509Enrollment::get_NameValuePairs
author: windows-sdk-content
description: Retrieves a collection of name-value pairs associated with the enrollment object.
old-location: security\ix509enrollment_namevaluepairs_property.htm
tech.root: SecCertEnroll
ms.assetid: d682fb7c-de80-4285-baa2-f86c997f0987
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509Enrollment interface [Security],NameValuePairs property, IX509Enrollment.NameValuePairs, IX509Enrollment.get_NameValuePairs, IX509Enrollment::NameValuePairs, IX509Enrollment::get_NameValuePairs, NameValuePairs property [Security], NameValuePairs property [Security],IX509Enrollment interface, certenroll/IX509Enrollment::NameValuePairs, certenroll/IX509Enrollment::get_NameValuePairs, get_NameValuePairs, security.ix509enrollment_namevaluepairs_property
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
 - IX509Enrollment.NameValuePairs
 - IX509Enrollment.get_NameValuePairs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Enrollment::get_NameValuePairs


## -description


The <b>NameValuePairs</b> property retrieves a collection of name-value pairs associated with the enrollment object.

This property is read-only.


## -parameters


## -remarks



name-value pairs are passed to the certification authority (CA) with the request for the CA to act upon. The <a href="https://msdn.microsoft.com/en-us/library/Aa378746(v=VS.85).aspx">IX509NameValuePairs</a> object is associated with the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> object when the object is initialized. Therefore, before calling this property, you must initialize the <b>IX509Enrollment</b> object by calling one of the following methods.<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378046(v=VS.85).aspx">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377872(v=VS.85).aspx">InitializeFromRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa378023(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a>
 

 

