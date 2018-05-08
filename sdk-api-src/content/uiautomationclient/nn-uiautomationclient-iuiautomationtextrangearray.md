---
UID: NN:uiautomationclient.IUIAutomationTextRangeArray
title: IUIAutomationTextRangeArray
author: windows-driver-content
description: Represents a collection of IUIAutomationTextRange objects.
old-location: winauto\uiauto_IUIAutomationTextRangeArray.htm
old-project: WinAuto
ms.assetid: 9f059173-7539-4164-b7af-182fa851d11a
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IUIAutomationTextRangeArray, IUIAutomationTextRangeArray interface [Windows Accessibility], IUIAutomationTextRangeArray interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTextRangeArray, uiauto_IUIAutomationTextRangeArray, uiautomationclient/IUIAutomationTextRangeArray, winauto.uiauto_IUIAutomationTextRangeArray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.dll
api_name:
-	IUIAutomationTextRangeArray
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextRangeArray interface


## -description


Represents a collection of <a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextRangeArray</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationTextRangeArray</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationTextRangeArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5077152-b06a-4391-a0c2-013362014b2b">GetElement</a>
</td>
<td align="left" width="63%">
Retrieves a text range from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextRangeArray</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/adbbff9d-dba8-4d37-8809-0e00ac39144c">Length</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of text ranges in the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

