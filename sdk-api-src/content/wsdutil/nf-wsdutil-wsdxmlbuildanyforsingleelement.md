---
UID: NF:wsdutil.WSDXMLBuildAnyForSingleElement
title: WSDXMLBuildAnyForSingleElement function
author: windows-sdk-content
description: Creates an XML element with a specified name and value.
old-location: ncd\wsdxmlbuildanyforsingleelement.htm
old-project: wsdapi
ms.assetid: 2a8b9b4a-0a08-442a-896f-f980bff28f03
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSDXMLBuildAnyForSingleElement, WSDXMLBuildAnyForSingleElement function, ncd.wsdxmlbuildanyforsingleelement, wsdutil/WSDXMLBuildAnyForSingleElement
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
tech.root: 
req.typenames: RESPONSEBODY_SubscriptionEnd
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDXMLBuildAnyForSingleElement
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSDXMLBuildAnyForSingleElement function


## -description


Creates an XML element with a specified name and value.  The created element can be used as the child of an XML <b>any</b>  element.


## -parameters




### -param pElementName [in]

Reference to a <a href="https://msdn.microsoft.com/9dce71d2-700c-4f86-9308-dee6a69010bb">WSDXML_NAME</a> structure that contains the name of the  created element.


### -param pszText [in]

The text value of the created element.


### -param ppAny [out]

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> that contains the created element.  <i>ppAny</i> must be freed with a call to <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a>.


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
<i>pElementName</i> is <b>NULL</b> or the length in characters of <i>pszText</i> exceeds WSD_MAX_TEXT_LENGTH (8192).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAny</i> is <b>NULL</b>.

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
 



