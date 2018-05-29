---
UID: NF:certenroll.ICertificatePolicy.get_ObjectId
title: ICertificatePolicy::get_ObjectId
author: windows-sdk-content
description: Retrieves an object identifier (OID) for the policy object.
old-location: security\icertificatepolicy_objectid_property.htm
old-project: SecCertEnroll
ms.assetid: 42d1689d-c086-4d67-8e16-997ecd515ae2
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ICertificatePolicy interface [Security],ObjectId property, ICertificatePolicy.ObjectId, ICertificatePolicy.get_ObjectId, ICertificatePolicy::ObjectId, ICertificatePolicy::get_ObjectId, ObjectId property [Security], ObjectId property [Security],ICertificatePolicy interface, certenroll/ICertificatePolicy::ObjectId, certenroll/ICertificatePolicy::get_ObjectId, get_ObjectId, security.icertificatepolicy_objectid_property
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
-	ICertificatePolicy.ObjectId
-	ICertificatePolicy.get_ObjectId
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertificatePolicy::get_ObjectId


## -description


The <b>ObjectId</b> property retrieves an object identifier (OID) for the policy object.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> object stores information about the OID internally in a CryptoAPI <a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a> structure. You cannot use this structure directly from the  Certificate Enrollment API, but you can use the  <b>IObjectId</b> interface to retrieve the display name or dotted decimal name of the OID, or the <a href="https://msdn.microsoft.com/30e8c740-854b-409f-a138-3871df305708">CERTENROLL_OBJECTID</a> value.




## -see-also




<a href="https://msdn.microsoft.com/2503adcb-0b73-42ef-98cf-a2b906e34ef7">ICertificatePolicies</a>



<a href="https://msdn.microsoft.com/2162de70-edcc-4f01-807d-79ff200d0016">ICertificatePolicy</a>
 

 

