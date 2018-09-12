---
UID: NF:certenroll.IAlternativeName.get_ObjectId
title: IAlternativeName::get_ObjectId
author: windows-sdk-content
description: Retrieves the object identifier (OID), if any, associated with the name.
old-location: security\ialternativename_objectid_property.htm
tech.root: SecCertEnroll
ms.assetid: be14756b-a7dc-40f4-ae09-b576f85837f6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAlternativeName interface [Security],ObjectId property, IAlternativeName.ObjectId, IAlternativeName.get_ObjectId, IAlternativeName::ObjectId, IAlternativeName::get_ObjectId, ObjectId property [Security], ObjectId property [Security],IAlternativeName interface, certenroll/IAlternativeName::ObjectId, certenroll/IAlternativeName::get_ObjectId, get_ObjectId, security.ialternativename_objectid_property
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
 - IAlternativeName.ObjectId
 - IAlternativeName.get_ObjectId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAlternativeName::get_ObjectId


## -description


The <b>ObjectId</b> property retrieves the  <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID), if any, associated with the name.

This property is read-only.


## -parameters


## -remarks



You can retrieve a value for this property if you initialized the <a href="https://msdn.microsoft.com/en-us/library/Aa374981(v=VS.85).aspx">IAlternativeName</a> object in any of the following ways:

<ul>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/Aa375017(v=VS.85).aspx">InitializeFromOtherName</a> and supply an OID.</li>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/Aa375021(v=VS.85).aspx">InitializeFromRawData</a> and specify the XCN_CERT_ALT_NAME_GUID type.</li>
<li>Call <a href="https://msdn.microsoft.com/en-us/library/Aa375024(v=VS.85).aspx">InitializeFromString</a> and specify the XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME type.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374981(v=VS.85).aspx">IAlternativeName</a>
 

 

