---
UID: NF:certenroll.ICertPropertyEnrollment.get_RequestId
title: ICertPropertyEnrollment::get_RequestId
author: windows-sdk-content
description: Retrieves a unique certificate request identifier.
old-location: security\icertpropertyenrollment_requestid_property.htm
tech.root: SecCertEnroll
ms.assetid: a9e2000c-7d64-43f1-b891-b5cd6f46201f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICertPropertyEnrollment interface [Security],RequestId property, ICertPropertyEnrollment.RequestId, ICertPropertyEnrollment.get_RequestId, ICertPropertyEnrollment::RequestId, ICertPropertyEnrollment::get_RequestId, RequestId property [Security], RequestId property [Security],ICertPropertyEnrollment interface, certenroll/ICertPropertyEnrollment::RequestId, certenroll/ICertPropertyEnrollment::get_RequestId, get_RequestId, security.icertpropertyenrollment_requestid_property
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
 - ICertPropertyEnrollment.RequestId
 - ICertPropertyEnrollment.get_RequestId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- ICertPropertyEnrollment.get_RequestId
: 
---

# ICertPropertyEnrollment::get_RequestId


## -description


The <b>RequestId</b> property retrieves a unique  certificate request identifier.

This property is read-only.


## -parameters


## -remarks



Set the  <b>RequestId</b> property by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa375690(v=VS.85).aspx">Initialize</a> method. The request ID is created during the enrollment process. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa378067(v=VS.85).aspx">RequestId</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> interface.

The ID can be used during subsequent communication between the client and the CA. For example, if a CA marks a request as pending when initially submitted, the client can use the request ID and the configuration string when it again contacts the CA and attempts to retrieve the certificate response.

You can also call the following properties to retrieve the other values specified during initialization:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375672(v=VS.85).aspx">CADnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375676(v=VS.85).aspx">CAName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375681(v=VS.85).aspx">FriendlyName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375665(v=VS.85).aspx">ICertPropertyEnrollment</a>
 

 

