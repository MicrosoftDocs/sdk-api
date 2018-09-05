---
UID: NF:wsdutil.WSDXMLAddChild
title: WSDXMLAddChild function
author: windows-sdk-content
description: Adds a child element.
old-location: ncd\wsdxmladdchild.htm
old-project: WsdApi
ms.assetid: a0688b03-6f91-4b8e-88d1-b40af69fe8bb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WSDXMLAddChild, WSDXMLAddChild function, ncd.wsdxmladdchild, wsdutil/WSDXMLAddChild
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wsdutil.h
req.include-header: Wsdapi.h
req.redist: 
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
 - WSDXMLAddChild
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSDXMLAddChild function


## -description


Adds a child element.


## -parameters




### -param pParent

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that contains the parent element.


### -param pChild

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that contains the child element.


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
<i>pParent</i> is <b>NULL</b>, <i>pChild</i> is <b>NULL</b>, <i>pChild</i> already has a parent, or a sibling could not be added to an existing child of <i>pParent</i>.

</td>
</tr>
</table>
 



