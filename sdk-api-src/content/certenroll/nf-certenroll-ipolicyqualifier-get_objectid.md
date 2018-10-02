---
UID: NF:certenroll.IPolicyQualifier.get_ObjectId
title: IPolicyQualifier::get_ObjectId
author: windows-sdk-content
description: Retrieves the object identifier (OID) for the qualifier.
old-location: security\ipolicyqualifier_objectid_property.htm
tech.root: SecCertEnroll
ms.assetid: d19efcd3-c5fc-4268-af39-2385b7babcc9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPolicyQualifier interface [Security],ObjectId property, IPolicyQualifier.ObjectId, IPolicyQualifier.get_ObjectId, IPolicyQualifier::ObjectId, IPolicyQualifier::get_ObjectId, ObjectId property [Security], ObjectId property [Security],IPolicyQualifier interface, certenroll/IPolicyQualifier::ObjectId, certenroll/IPolicyQualifier::get_ObjectId, get_ObjectId, security.ipolicyqualifier_objectid_property
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
 - IPolicyQualifier.ObjectId
 - IPolicyQualifier.get_ObjectId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPolicyQualifier::get_ObjectId


## -description


The <b>ObjectId</b> property retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for the qualifier.

This property is read-only.


## -parameters


## -remarks



If you specified <b>PolicyQualifierTypeUrl</b> in the <i>Type</i> parameter of the <a href="https://msdn.microsoft.com/fc8b5916-0557-4f9b-8478-169a3dd9cebc">InitializeEncode</a> method,  <b>XCN_OID_PKIX_POLICY_QUALIFIER_CPS</b> (1.3.6.1.5.5.7.2.1)  is returned. If you specified <b>PolicyQualifierTypeUserNotice</b>,  <b>XCN_OID_PKIX_POLICY_QUALIFIER_USERNOTICE</b> (1.3.6.1.5.5.7.2.2)  is returned.

You must call  <a href="https://msdn.microsoft.com/fc8b5916-0557-4f9b-8478-169a3dd9cebc">InitializeEncode</a> to initialize the qualifier object before you can retrieve this property. You can also retrieve the following properties for this object:<ul>
<li>The <a href="https://msdn.microsoft.com/73cecc9b-519c-45c8-b9f8-864ff628560a">Qualifier</a> property retrieves the string specified for the <i>strQualifier</i> parameter of the <a href="https://msdn.microsoft.com/fc8b5916-0557-4f9b-8478-169a3dd9cebc">InitializeEncode</a> method.</li>
<li>The <a href="https://msdn.microsoft.com/a654f60c-7f67-4fe2-847b-e8c5f91fde80">RawData</a> property retrieves the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded qualifier.</li>
<li>The <a href="https://msdn.microsoft.com/eb48d2a0-c689-45b1-9f06-83df71987b4b">Type</a> property retrieves a value of the <a href="https://msdn.microsoft.com/76cd1874-b80d-466e-9c7d-12cf8d310b8a">PolicyQualifierType</a> enumeration that specifies the qualifier type.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/3804e372-17bb-458d-8da5-85d760fe5e60">IPolicyQualifier</a>
 

 

