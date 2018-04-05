---
UID: NF:wsdutil.WSDXMLAddSibling
title: WSDXMLAddSibling function
author: windows-driver-content
description: Adds a sibling element.
old-location: ncd\wsdxmladdsibling.htm
old-project: WsdApi
ms.assetid: dbe5de39-eb8e-4352-b0c4-32d10e324185
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WSDXMLAddSibling, WSDXMLAddSibling function, ncd.wsdxmladdsibling, wsdutil/WSDXMLAddSibling
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	WSDXMLAddSibling
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSDXMLAddSibling function


## -description


Adds a sibling element.


## -parameters




### -param pFirst [in]

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that contains the first sibling.


### -param pSecond [in]

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that contains the second sibling.


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
<i>pFirst</i> or <i>pSecond</i> is <b>NULL</b>.

</td>
</tr>
</table>
 



