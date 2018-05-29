---
UID: NF:certenroll.IAlternativeName.get_RawData
title: IAlternativeName::get_RawData
author: windows-sdk-content
description: Retrieves the Distinguished Encoding Rules (DER) encoded byte array that contains the name.
old-location: security\ialternativename_rawdata_property.htm
old-project: SecCertEnroll
ms.assetid: 7385654d-03f8-4796-a95c-000fa8ab65a3
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IAlternativeName interface [Security],RawData property, IAlternativeName.RawData, IAlternativeName.get_RawData, IAlternativeName::RawData, IAlternativeName::get_RawData, RawData property [Security], RawData property [Security],IAlternativeName interface, certenroll/IAlternativeName::RawData, certenroll/IAlternativeName::get_RawData, get_RawData, security.ialternativename_rawdata_property
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
-	IAlternativeName.RawData
-	IAlternativeName.get_RawData
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IAlternativeName::get_RawData


## -description


The <b>RawData</b> property retrieves the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the name. The byte array is contained in a Unicode encoded string.

This property is read-only.


## -parameters


## -remarks



You can retrieve a value for this property if you initialized the <a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a> object in any of the following ways:

<ul>
<li>Call <a href="https://msdn.microsoft.com/cd697085-0e8e-4a18-a7c5-77cd4927f664">InitializeFromOtherName</a> and supply an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).</li>
<li>Call <a href="https://msdn.microsoft.com/1559801c-ec62-471e-851f-f67219565cd1">InitializeFromRawData</a> and specify the XCN_CERT_ALT_NAME_GUID,  XCN_CERT_ALT_NAME_DIRECTORY_NAME, or XCN_CERT_ALT_NAME_IP_ADDRESS types.</li>
<li>Call <a href="https://msdn.microsoft.com/7b5f7dd3-00dc-474b-8920-45a3acded209">InitializeFromString</a> and specify the XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME type.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a>
 

 

