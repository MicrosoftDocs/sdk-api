---
UID: NF:certenroll.ICspInformation.get_Valid
title: ICspInformation::get_Valid
author: windows-driver-content
description: Retrieves a Boolean value that specifies whether the provider is installed on the client computer.
old-location: security\icspinformation_valid_property.htm
old-project: SecCertEnroll
ms.assetid: 507896b0-598c-4a2d-854e-d4d266fdfaf7
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICspInformation interface [Security],Valid property, ICspInformation.Valid, ICspInformation.get_Valid, ICspInformation::Valid, ICspInformation::get_Valid, Valid property [Security], Valid property [Security],ICspInformation interface, certenroll/ICspInformation::Valid, certenroll/ICspInformation::get_Valid, get_Valid, security.icspinformation_valid_property
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
-	ICspInformation.Valid
-	ICspInformation.get_Valid
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformation::get_Valid


## -description


The <b>Valid</b> property retrieves a Boolean value that specifies whether the provider is installed on the client computer.

This property is read-only.


## -parameters


## -remarks



The <b>Valid</b> property is typically set by the Certificate Enrollment Control when it processes the list of providers identified in a template-based certificate request. If a provider listed in the template is not installed on the client, the control creates an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object and sets the value of this property to false. You can use this property value in a user interface to indicate whether a provider is available. If a provider is not installed, only the <b>Valid</b> property and the <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> property provide meaningful information.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
 

 

