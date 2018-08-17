---
UID: NF:certenroll.ICertPropertyEnrollment.get_CAName
title: ICertPropertyEnrollment::get_CAName
author: windows-sdk-content
description: Retrieves the common name (CN) of the certification authority (CA).
old-location: security\icertpropertyenrollment_caname_property.htm
old-project: seccertenroll
ms.assetid: ea490e37-e1b9-4887-8051-c3447136875c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CAName property [Security], CAName property [Security],ICertPropertyEnrollment interface, ICertPropertyEnrollment interface [Security],CAName property, ICertPropertyEnrollment.CAName, ICertPropertyEnrollment.get_CAName, ICertPropertyEnrollment::CAName, ICertPropertyEnrollment::get_CAName, certenroll/ICertPropertyEnrollment::CAName, certenroll/ICertPropertyEnrollment::get_CAName, get_CAName, security.icertpropertyenrollment_caname_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - ICertPropertyEnrollment.CAName
 - ICertPropertyEnrollment.get_CAName
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyEnrollment::get_CAName


## -description


The <b>CAName</b> property retrieves the common name (CN) of the certification authority (CA).

This property is read-only.


## -parameters


## -remarks



Set the  <b>CAName</b> property by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa375690(v=VS.85).aspx">Initialize</a> method. The common name is returned to the client during the enrollment process and is part of the certification authority  configuration string. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa377864(v=VS.85).aspx">CAConfigString</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> interface.

You can also call the following properties to retrieve the other values specified during initialization:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375672(v=VS.85).aspx">CADnsName</a>
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
 

 

