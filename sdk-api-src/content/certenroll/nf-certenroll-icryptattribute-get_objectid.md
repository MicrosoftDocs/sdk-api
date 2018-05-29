---
UID: NF:certenroll.ICryptAttribute.get_ObjectId
title: ICryptAttribute::get_ObjectId
author: windows-sdk-content
description: Retrieves the object identifier (OID) for the attribute.
old-location: security\icryptattribute_objectid_property.htm
old-project: SecCertEnroll
ms.assetid: 9ae9a217-1658-42ac-bd28-33abab5d0d70
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ICryptAttribute interface [Security],ObjectId property, ICryptAttribute.ObjectId, ICryptAttribute.get_ObjectId, ICryptAttribute::ObjectId, ICryptAttribute::get_ObjectId, ObjectId property [Security], ObjectId property [Security],ICryptAttribute interface, certenroll/ICryptAttribute::ObjectId, certenroll/ICryptAttribute::get_ObjectId, get_ObjectId, security.icryptattribute_objectid_property
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
-	ICryptAttribute.ObjectId
-	ICryptAttribute.get_ObjectId
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICryptAttribute::get_ObjectId


## -description


The <b>ObjectId</b> property retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for the attribute.

This property is read-only.


## -parameters


## -remarks



 You can initialize an <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> object by calling <a href="https://msdn.microsoft.com/dce84308-aecc-4841-88da-e948313b90b3">InitializeFromName</a>. This method initializes the object by using a value from the <a href="https://msdn.microsoft.com/30e8c740-854b-409f-a138-3871df305708">CERTENROLL_OBJECTID</a> enumeration. The enumeration value is associated with an ASN.1 object identifier. For example, the value <b>XCN_OID_COUNTRY_NAME</b> is associated with a string containing 2.5.4.6. This is the dotted decimal representation of the joint-iso-itu-t(2)ds(5)attributeType(4)countryName(6) object identifier.




## -see-also




<a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>



<a href="https://msdn.microsoft.com/dd891506-f25b-4aa5-b739-0d66d5a5f395">IX509Attributes</a>
 

 

