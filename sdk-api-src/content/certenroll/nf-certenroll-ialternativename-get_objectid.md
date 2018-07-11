---
UID: NF:certenroll.IAlternativeName.get_ObjectId
title: IAlternativeName::get_ObjectId
author: windows-sdk-content
description: Retrieves the object identifier (OID), if any, associated with the name.
old-location: security\ialternativename_objectid_property.htm
old-project: seccertenroll
ms.assetid: be14756b-a7dc-40f4-ae09-b576f85837f6
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IAlternativeName interface [Security],ObjectId property, IAlternativeName.ObjectId, IAlternativeName.get_ObjectId, IAlternativeName::ObjectId, IAlternativeName::get_ObjectId, ObjectId property [Security], ObjectId property [Security],IAlternativeName interface, certenroll/IAlternativeName::ObjectId, certenroll/IAlternativeName::get_ObjectId, get_ObjectId, security.ialternativename_objectid_property
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IAlternativeName.ObjectId
 - IAlternativeName.get_ObjectId
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IAlternativeName::get_ObjectId


## -description


The <b>ObjectId</b> property retrieves the  <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID), if any, associated with the name.

This property is read-only.


## -parameters


## -remarks



You can retrieve a value for this property if you initialized the <a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a> object in any of the following ways:

<ul>
<li>Call <a href="https://msdn.microsoft.com/cd697085-0e8e-4a18-a7c5-77cd4927f664">InitializeFromOtherName</a> and supply an OID.</li>
<li>Call <a href="https://msdn.microsoft.com/1559801c-ec62-471e-851f-f67219565cd1">InitializeFromRawData</a> and specify the XCN_CERT_ALT_NAME_GUID type.</li>
<li>Call <a href="https://msdn.microsoft.com/7b5f7dd3-00dc-474b-8920-45a3acded209">InitializeFromString</a> and specify the XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME type.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a>
 

 

