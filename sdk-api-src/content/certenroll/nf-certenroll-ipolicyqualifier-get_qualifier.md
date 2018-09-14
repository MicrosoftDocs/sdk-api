---
UID: NF:certenroll.IPolicyQualifier.get_Qualifier
title: IPolicyQualifier::get_Qualifier
author: windows-sdk-content
description: Retrieves a string that contains the qualifier used to initialize the object.
old-location: security\ipolicyqualifier_qualifier_property.htm
tech.root: seccertenroll
ms.assetid: 73cecc9b-519c-45c8-b9f8-864ff628560a
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IPolicyQualifier interface [Security],Qualifier property, IPolicyQualifier.Qualifier, IPolicyQualifier.get_Qualifier, IPolicyQualifier::Qualifier, IPolicyQualifier::get_Qualifier, Qualifier property [Security], Qualifier property [Security],IPolicyQualifier interface, certenroll/IPolicyQualifier::Qualifier, certenroll/IPolicyQualifier::get_Qualifier, get_Qualifier, security.ipolicyqualifier_qualifier_property
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
 - IPolicyQualifier.Qualifier
 - IPolicyQualifier.get_Qualifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPolicyQualifier::get_Qualifier


## -description


The <b>Qualifier</b> property retrieves a string that contains the qualifier used to initialize the object.

This property is read-only.


## -parameters


## -remarks



You must call  <a href="https://msdn.microsoft.com/en-us/library/Aa376813(v=VS.85).aspx">InitializeEncode</a> to initialize the qualifier object before you can retrieve this property. The value retrieved is the string entered in the <i>strQualifier</i> parameter of that method. You can also retrieve the following properties for this object:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376815(v=VS.85).aspx">ObjectId</a> property retrieves an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) that identifies whether the qualifier is a CPS or a user notice.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376818(v=VS.85).aspx">RawData</a> property retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded qualifier.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376819(v=VS.85).aspx">Type</a> property retrieves a value of the <a href="https://msdn.microsoft.com/en-us/library/Aa379084(v=VS.85).aspx">PolicyQualifierType</a> enumeration that specifies the qualifier type.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376803(v=VS.85).aspx">IPolicyQualifier</a>
 

 

