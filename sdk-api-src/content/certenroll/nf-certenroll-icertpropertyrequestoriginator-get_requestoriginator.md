---
UID: NF:certenroll.ICertPropertyRequestOriginator.get_RequestOriginator
title: ICertPropertyRequestOriginator::get_RequestOriginator
author: windows-sdk-content
description: Retrieves a string that contains the DNS name of the originating computer.
old-location: security\icertpropertyrequestoriginator_requestoriginator_property.htm
old-project: SecCertEnroll
ms.assetid: 0ac6b8da-9183-4683-a172-a9742b40da64
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ICertPropertyRequestOriginator interface [Security],RequestOriginator property, ICertPropertyRequestOriginator.RequestOriginator, ICertPropertyRequestOriginator.get_RequestOriginator, ICertPropertyRequestOriginator::RequestOriginator, ICertPropertyRequestOriginator::get_RequestOriginator, RequestOriginator property [Security], RequestOriginator property [Security],ICertPropertyRequestOriginator interface, certenroll/ICertPropertyRequestOriginator::RequestOriginator, certenroll/ICertPropertyRequestOriginator::get_RequestOriginator, get_RequestOriginator, security.icertpropertyrequestoriginator_requestoriginator_property
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ICertPropertyRequestOriginator.RequestOriginator
-	ICertPropertyRequestOriginator.get_RequestOriginator
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyRequestOriginator::get_RequestOriginator


## -description


The <b>RequestOriginator</b> property retrieves a string that contains the DNS name of the originating computer.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method or the <a href="https://msdn.microsoft.com/466e0767-d13a-4f5d-9715-47bb7b9d4142">InitializeFromLocalRequestOriginator</a> method to specify a value for the <b>RequestOriginator</b> property.




## -see-also




<a href="https://msdn.microsoft.com/ce33605e-c3ae-4b96-a13e-6f06e8d5ffee">ICertPropertyRequestOriginator</a>
 

 

