---
UID: NF:wsdbase.IWSDAddress.Deserialize
title: IWSDAddress::Deserialize
author: windows-sdk-content
description: Parses the address, validates its component parts and saves them in the object.
old-location: ncd\iwsdaddress_deserialize.htm
old-project: WsdApi
ms.assetid: a23ac1cd-d2af-4562-a623-64ca1deb1830
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: Deserialize, Deserialize method, Deserialize method,IWSDAddress interface, IWSDAddress interface,Deserialize method, IWSDAddress.Deserialize, IWSDAddress::Deserialize, ncd.iwsdaddress_deserialize, wsdbase/IWSDAddress::Deserialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wsdapi.dll
api_name:
-	IWSDAddress.Deserialize
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDAddress::Deserialize


## -description


Parses the address, validates its component parts and saves them in the object.


## -parameters




### -param pszBuffer [in]

Address to save in the object.


## -returns



Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszBuffer</i> is <b>NULL</b>, its length in characters exceeds WSD_MAX_TEXT_LENGTH (8192), or it does not contain an address in a valid format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a>
 

 

