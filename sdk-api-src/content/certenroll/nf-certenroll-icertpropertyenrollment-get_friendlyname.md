---
UID: NF:certenroll.ICertPropertyEnrollment.get_FriendlyName
title: ICertPropertyEnrollment::get_FriendlyName (certenroll.h)
author: windows-sdk-content
description: Retrieves the display name of the certificate.
old-location: security\icertpropertyenrollment_friendlyname_property.htm
tech.root: seccertenroll
ms.assetid: a12b7368-cace-47c4-bfd4-08845dc2634c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FriendlyName property [Security], FriendlyName property [Security],ICertPropertyEnrollment interface, ICertPropertyEnrollment interface [Security],FriendlyName property, ICertPropertyEnrollment.FriendlyName, ICertPropertyEnrollment.get_FriendlyName, ICertPropertyEnrollment::FriendlyName, ICertPropertyEnrollment::get_FriendlyName, certenroll/ICertPropertyEnrollment::FriendlyName, certenroll/ICertPropertyEnrollment::get_FriendlyName, get_FriendlyName, security.icertpropertyenrollment_friendlyname_property
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
ms.custom: 19H1
---

# ICertPropertyEnrollment::get_FriendlyName


## -description


The <b>FriendlyName</b> property retrieves the display name of the certificate.

This property is read-only.


## -parameters


## -remarks



Set the  <b>FriendlyName</b> property by calling the <a href="https://msdn.microsoft.com/47e9b11f-3f23-4e2f-817a-4b6311e3d710">Initialize</a> method. The display name is specified during the enrollment process. For more information, see the <a href="https://msdn.microsoft.com/35c3eea1-2a3a-4e13-9232-f40429669948">CertificateFriendlyName</a> property on the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> interface.

You can also call the following properties to retrieve the other values specified during initialization:<ul>
<li>
<a href="https://msdn.microsoft.com/5b388cfe-e0b1-4b57-bf6c-81f9ab65ffcf">CADnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ea490e37-e1b9-4887-8051-c3447136875c">CAName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a9e2000c-7d64-43f1-b891-b5cd6f46201f">RequestId</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>



<a href="https://msdn.microsoft.com/7530998b-b59c-426b-a74a-ead4bca55c3b">ICertPropertyEnrollment</a>
 

 

