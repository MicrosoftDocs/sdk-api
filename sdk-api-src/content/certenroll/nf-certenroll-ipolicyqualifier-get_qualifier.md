---
UID: NF:certenroll.IPolicyQualifier.get_Qualifier
title: IPolicyQualifier::get_Qualifier
author: windows-sdk-content
description: Retrieves a string that contains the qualifier used to initialize the object.
old-location: security\ipolicyqualifier_qualifier_property.htm
old-project: SecCertEnroll
ms.assetid: 73cecc9b-519c-45c8-b9f8-864ff628560a
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IPolicyQualifier interface [Security],Qualifier property, IPolicyQualifier.Qualifier, IPolicyQualifier.get_Qualifier, IPolicyQualifier::Qualifier, IPolicyQualifier::get_Qualifier, Qualifier property [Security], Qualifier property [Security],IPolicyQualifier interface, certenroll/IPolicyQualifier::Qualifier, certenroll/IPolicyQualifier::get_Qualifier, get_Qualifier, security.ipolicyqualifier_qualifier_property
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
-	IPolicyQualifier.Qualifier
-	IPolicyQualifier.get_Qualifier
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IPolicyQualifier::get_Qualifier


## -description


The <b>Qualifier</b> property retrieves a string that contains the qualifier used to initialize the object.

This property is read-only.


## -parameters


## -remarks



You must call  <a href="https://msdn.microsoft.com/fc8b5916-0557-4f9b-8478-169a3dd9cebc">InitializeEncode</a> to initialize the qualifier object before you can retrieve this property. The value retrieved is the string entered in the <i>strQualifier</i> parameter of that method. You can also retrieve the following properties for this object:<ul>
<li>The <a href="https://msdn.microsoft.com/d19efcd3-c5fc-4268-af39-2385b7babcc9">ObjectId</a> property retrieves an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) that identifies whether the qualifier is a CPS or a user notice.</li>
<li>The <a href="https://msdn.microsoft.com/a654f60c-7f67-4fe2-847b-e8c5f91fde80">RawData</a> property retrieves the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded qualifier.</li>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property retrieves a value of the <a href="https://msdn.microsoft.com/76cd1874-b80d-466e-9c7d-12cf8d310b8a">PolicyQualifierType</a> enumeration that specifies the qualifier type.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/3804e372-17bb-458d-8da5-85d760fe5e60">IPolicyQualifier</a>
 

 

