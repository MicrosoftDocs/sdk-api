---
UID: NN:uiautomationclient.IUIAutomationTextRange3
title: IUIAutomationTextRange3
author: windows-sdk-content
description: Extends the IUIAutomationTextRange2 interface to support faster access to the underlying rich text data on a text range.
old-location: winauto\uiauto_IUIAutomationTextRange3.htm
tech.root: WinAuto
ms.assetid: 3491996E-89EF-496D-94B6-FF8D121D3828
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IUIAutomationTextRange3, IUIAutomationTextRange3 interface [Windows Accessibility], IUIAutomationTextRange3 interface [Windows Accessibility],described, uiautomationclient/IUIAutomationTextRange3, winauto.uiauto_IUIAutomationTextRange3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationTextRange3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextRange3 interface


## -description


Extends the <a href="https://msdn.microsoft.com/62E95500-5691-FAE8-BC31-0BB31318D8A4">IUIAutomationTextRange2</a> interface to support faster access to the underlying rich text data on a text range.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextRange3</b> interface inherits from <a href="https://msdn.microsoft.com/62E95500-5691-FAE8-BC31-0BB31318D8A4">IUIAutomationTextRange2</a>. <b>IUIAutomationTextRange3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationTextRange3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1AF29BF1-A074-4054-B338-7B6922B1415C">GetAttributeValues</a>
</td>
<td align="left" width="63%">
Returns all of the requested text attribute values for a text range in a single cross-process call.  This is equivalent to calling <a href="https://msdn.microsoft.com/7a77774e-7be0-473e-a0c9-e1aa108549e1">GetAttributeValue</a>, except it can retrieve multiple values instead of just one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1C8F0E81-ED73-4752-BD27-7981508671D0">GetChildrenBuildCache</a>
</td>
<td align="left" width="63%">
Returns the children and supplied properties and patterns for elements in a text range in a single cross-process call.  This is equivalent to calling <a href="https://msdn.microsoft.com/714e9d91-c6b9-4fa2-8a14-9bdd721b3135">GetChildren</a>, but adds the standard build cache pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6F5BC5DB-F9C0-40DF-8E29-FFACFBCAD80F">GetEnclosingElementBuildCache</a>
</td>
<td align="left" width="63%">
Gets the enclosing element and supplied properties and patterns for an element in a text range in a single cross-process call.  This is equivalent to calling <a href="https://msdn.microsoft.com/0120b4af-6f08-4bbd-b649-0f8e84cda3b9">GetEnclosingElement</a>, but adds the standard build cache pattern.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/62E95500-5691-FAE8-BC31-0BB31318D8A4">IUIAutomationTextRange2</a>
 

 

