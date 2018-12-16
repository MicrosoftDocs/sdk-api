---
UID: NF:certenroll.IPolicyQualifier.get_RawData
title: IPolicyQualifier::get_RawData
author: windows-sdk-content
description: Retrieves the Distinguished Encoding Rules (DER) encoded qualifier object.
old-location: security\ipolicyqualifier_rawdata_property.htm
tech.root: seccertenroll
ms.assetid: a654f60c-7f67-4fe2-847b-e8c5f91fde80
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPolicyQualifier interface [Security],RawData property, IPolicyQualifier.RawData, IPolicyQualifier.get_RawData, IPolicyQualifier::RawData, IPolicyQualifier::get_RawData, RawData property [Security], RawData property [Security],IPolicyQualifier interface, certenroll/IPolicyQualifier::RawData, certenroll/IPolicyQualifier::get_RawData, get_RawData, security.ipolicyqualifier_rawdata_property
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
 - IPolicyQualifier.RawData
 - IPolicyQualifier.get_RawData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPolicyQualifier::get_RawData


## -description


The <b>RawData</b> property retrieves the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded qualifier object.

This property is read-only.


## -parameters


## -remarks



You must call  <a href="https://msdn.microsoft.com/fc8b5916-0557-4f9b-8478-169a3dd9cebc">InitializeEncode</a> to initialize the qualifier object before you can retrieve this property. The value retrieved is the DER-encoded byte array that contains the qualifier. The byte array is represented as a string. You can use the <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration to apply Unicode encoding to the string.

You can also retrieve the following properties for this object:<ul>
<li>The <a href="https://msdn.microsoft.com/d19efcd3-c5fc-4268-af39-2385b7babcc9">ObjectId</a> property retrieves an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) that identifies whether the qualifier is a CPS or a user notice.</li>
<li>The <a href="https://msdn.microsoft.com/73cecc9b-519c-45c8-b9f8-864ff628560a">Qualifier</a> property retrieves the string specified for the <i>strQualifier</i> parameter of the <a href="https://msdn.microsoft.com/fc8b5916-0557-4f9b-8478-169a3dd9cebc">InitializeEncode</a> method.</li>
<li>The <a href="https://msdn.microsoft.com/eb48d2a0-c689-45b1-9f06-83df71987b4b">Type</a> property retrieves a value of the <a href="https://msdn.microsoft.com/76cd1874-b80d-466e-9c7d-12cf8d310b8a">PolicyQualifierType</a> enumeration that specifies the qualifier type.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/3804e372-17bb-458d-8da5-85d760fe5e60">IPolicyQualifier</a>
 

 

