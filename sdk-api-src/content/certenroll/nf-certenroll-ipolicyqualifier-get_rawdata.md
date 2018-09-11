---
UID: NF:certenroll.IPolicyQualifier.get_RawData
title: IPolicyQualifier::get_RawData
author: windows-sdk-content
description: Retrieves the Distinguished Encoding Rules (DER) encoded qualifier object.
old-location: security\ipolicyqualifier_rawdata_property.htm
tech.root: SecCertEnroll
ms.assetid: a654f60c-7f67-4fe2-847b-e8c5f91fde80
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPolicyQualifier interface [Security],RawData property, IPolicyQualifier.RawData, IPolicyQualifier.get_RawData, IPolicyQualifier::RawData, IPolicyQualifier::get_RawData, RawData property [Security], RawData property [Security],IPolicyQualifier interface, certenroll/IPolicyQualifier::RawData, certenroll/IPolicyQualifier::get_RawData, get_RawData, security.ipolicyqualifier_rawdata_property
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
 - IPolicyQualifier.RawData
 - IPolicyQualifier.get_RawData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPolicyQualifier::get_RawData


## -description


The <b>RawData</b> property retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded qualifier object.

This property is read-only.


## -parameters


## -remarks



You must call  <a href="https://msdn.microsoft.com/en-us/library/Aa376813(v=VS.85).aspx">InitializeEncode</a> to initialize the qualifier object before you can retrieve this property. The value retrieved is the DER-encoded byte array that contains the qualifier. The byte array is represented as a string. You can use the <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration to apply Unicode encoding to the string.

You can also retrieve the following properties for this object:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376815(v=VS.85).aspx">ObjectId</a> property retrieves an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) that identifies whether the qualifier is a CPS or a user notice.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376817(v=VS.85).aspx">Qualifier</a> property retrieves the string specified for the <i>strQualifier</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/Aa376813(v=VS.85).aspx">InitializeEncode</a> method.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376819(v=VS.85).aspx">Type</a> property retrieves a value of the <a href="https://msdn.microsoft.com/en-us/library/Aa379084(v=VS.85).aspx">PolicyQualifierType</a> enumeration that specifies the qualifier type.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376803(v=VS.85).aspx">IPolicyQualifier</a>
 

 

