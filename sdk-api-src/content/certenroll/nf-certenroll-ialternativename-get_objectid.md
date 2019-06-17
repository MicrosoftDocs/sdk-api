---
UID: NF:certenroll.IAlternativeName.get_ObjectId
title: IAlternativeName::get_ObjectId (certenroll.h)
author: windows-sdk-content
description: Retrieves the object identifier (OID), if any, associated with the name.
old-location: security\ialternativename_objectid_property.htm
tech.root: seccertenroll
ms.assetid: be14756b-a7dc-40f4-ae09-b576f85837f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAlternativeName interface [Security],ObjectId property, IAlternativeName.ObjectId, IAlternativeName.get_ObjectId, IAlternativeName::ObjectId, IAlternativeName::get_ObjectId, ObjectId property [Security], ObjectId property [Security],IAlternativeName interface, certenroll/IAlternativeName::ObjectId, certenroll/IAlternativeName::get_ObjectId, get_ObjectId, security.ialternativename_objectid_property
ms.topic: method
f1_keywords: ["certenroll/IAlternativeName.ObjectId"]
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
 - IAlternativeName.ObjectId
 - IAlternativeName.get_ObjectId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAlternativeName::get_ObjectId


## -description


The <b>ObjectId</b> property retrieves the  <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID), if any, associated with the name.

This property is read-only.


## -parameters


## -remarks



You can retrieve a value for this property if you initialized the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a> object in any of the following ways:

<ul>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromothername">InitializeFromOtherName</a> and supply an OID.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromrawdata">InitializeFromRawData</a> and specify the XCN_CERT_ALT_NAME_GUID type.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromstring">InitializeFromString</a> and specify the XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME type.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ialternativename">IAlternativeName</a>
 

 

