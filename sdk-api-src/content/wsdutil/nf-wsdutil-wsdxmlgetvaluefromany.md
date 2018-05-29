---
UID: NF:wsdutil.WSDXMLGetValueFromAny
title: WSDXMLGetValueFromAny function
author: windows-sdk-content
description: Retrieves a text value from a specified child element of an XML any element.
old-location: ncd\wsdxmlgetvaluefromany.htm
old-project: WsdApi
ms.assetid: 544399f6-d98d-4a57-824a-b21567262141
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSDXMLGetValueFromAny, WSDXMLGetValueFromAny function, ncd.wsdxmlgetvaluefromany, wsdutil/WSDXMLGetValueFromAny
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wsdutil.h
req.include-header: Wsdapi.h
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
req.typenames: RESPONSEBODY_SubscriptionEnd
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wsdapi.dll
api_name:
-	WSDXMLGetValueFromAny
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSDXMLGetValueFromAny function


## -description


Retrieves a text value from a specified child element of an XML <b>any</b> element. 


## -parameters




### -param pszNamespace [in]

The namespace of the element to retrieve.


### -param pszName [in]

The name of the element to retrieve.


### -param pAny [in]

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that contains the <b>any</b> element that is the parent of the element to retrieve.


### -param ppszValue [out]

The text value of the element specified by <i>pszNamespace</i> and <i>pszName</i>.  The memory usage of <i>ppszValue</i> is managed elsewhere.  Consequently, the calling application should not attempt to deallocate <i>ppszValue</i>.


## -returns



This function can return one of these values.

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
The length in characters of <i>pszNamespace</i> or <i>pszName</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or <i>pAny</i> is <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppszValue</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 



