---
UID: NN:fhcfg.IFhTarget
title: IFhTarget
author: windows-sdk-content
description: The IFhTarget interface allows client applications to read numeric and string properties of a File History backup target.
old-location: winprog\ifhtarget.htm
old-project: DevNotes
ms.assetid: 5A73A81A-72A3-4794-86E5-9CA8FCA200C0
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IFhTarget, IFhTarget interface [Windows API], IFhTarget interface [Windows API],described, fhcfg/IFhTarget, winprog.ifhtarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fhcfg.h
api_name:
-	IFhTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFhTarget interface


## -description


The <b>IFhTarget</b> interface allows client applications to read numeric and string properties of a File History backup target.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFhTarget</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFhTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFhTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3FA2F3AB-A406-4F19-AA5A-0D5596F1BF2C">GetNumericalProperty</a>
</td>
<td align="left" width="63%">
Retrieves a numeric property of the File History backup target that is represented by an <b>IFhTarget</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC5FE023-FA6E-4B97-AD9D-830975A17159">GetStringProperty</a>
</td>
<td align="left" width="63%">
Retrieves a string property of the File History backup target that is represented by an <b>IFhTarget</b> interface.

</td>
</tr>
</table> 

