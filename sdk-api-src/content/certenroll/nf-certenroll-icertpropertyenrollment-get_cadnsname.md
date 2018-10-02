---
UID: NF:certenroll.ICertPropertyEnrollment.get_CADnsName
title: ICertPropertyEnrollment::get_CADnsName
author: windows-sdk-content
description: Retrieves the Domain Naming System (DNS) name of the certification authority (CA).
old-location: security\icertpropertyenrollment_cadnsname_property.htm
tech.root: SecCertEnroll
ms.assetid: 5b388cfe-e0b1-4b57-bf6c-81f9ab65ffcf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CADnsName property [Security], CADnsName property [Security],ICertPropertyEnrollment interface, ICertPropertyEnrollment interface [Security],CADnsName property, ICertPropertyEnrollment.CADnsName, ICertPropertyEnrollment.get_CADnsName, ICertPropertyEnrollment::CADnsName, ICertPropertyEnrollment::get_CADnsName, certenroll/ICertPropertyEnrollment::CADnsName, certenroll/ICertPropertyEnrollment::get_CADnsName, get_CADnsName, security.icertpropertyenrollment_cadnsname_property
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
 - ICertPropertyEnrollment.CADnsName
 - ICertPropertyEnrollment.get_CADnsName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyEnrollment::get_CADnsName


## -description


The <b>CADnsName</b> property retrieves the Domain Naming System (DNS) name of the certification authority (CA).

This property is read-only.


## -parameters


## -remarks



Set the  <b>CADnsName</b> property by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa375690(v=VS.85).aspx">Initialize</a> method. The DNS name is returned to the client during the enrollment process and is part of the CA  configuration string. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa377864(v=VS.85).aspx">CAConfigString</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> interface.

You can also call the following properties to retrieve the other values specified during initialization:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375676(v=VS.85).aspx">CAName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375681(v=VS.85).aspx">FriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375707(v=VS.85).aspx">RequestId</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375665(v=VS.85).aspx">ICertPropertyEnrollment</a>
 

 

