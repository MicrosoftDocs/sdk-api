---
UID: NF:certenroll.ICertPropertyEnrollment.get_FriendlyName
title: ICertPropertyEnrollment::get_FriendlyName
author: windows-sdk-content
description: Retrieves the display name of the certificate.
old-location: security\icertpropertyenrollment_friendlyname_property.htm
tech.root: seccertenroll
ms.assetid: a12b7368-cace-47c4-bfd4-08845dc2634c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FriendlyName property [Security], FriendlyName property [Security],ICertPropertyEnrollment interface, ICertPropertyEnrollment interface [Security],FriendlyName property, ICertPropertyEnrollment.FriendlyName, ICertPropertyEnrollment.get_FriendlyName, ICertPropertyEnrollment::FriendlyName, ICertPropertyEnrollment::get_FriendlyName, certenroll/ICertPropertyEnrollment::FriendlyName, certenroll/ICertPropertyEnrollment::get_FriendlyName, get_FriendlyName, security.icertpropertyenrollment_friendlyname_property
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
 - ICertPropertyEnrollment.FriendlyName
 - ICertPropertyEnrollment.get_FriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyEnrollment::get_FriendlyName


## -description


The <b>FriendlyName</b> property retrieves the display name of the certificate.

This property is read-only.


## -parameters


## -remarks



Set the  <b>FriendlyName</b> property by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa375690(v=VS.85).aspx">Initialize</a> method. The display name is specified during the enrollment process. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa377866(v=VS.85).aspx">CertificateFriendlyName</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa377809(v=VS.85).aspx">IX509Enrollment</a> interface.

You can also call the following properties to retrieve the other values specified during initialization:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375672(v=VS.85).aspx">CADnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375676(v=VS.85).aspx">CAName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375707(v=VS.85).aspx">RequestId</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375665(v=VS.85).aspx">ICertPropertyEnrollment</a>
 

 

