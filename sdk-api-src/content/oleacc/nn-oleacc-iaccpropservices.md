---
UID: NN:oleacc.IAccPropServices
title: IAccPropServices
author: windows-sdk-content
description: Exposes methods for annotating accessible elements and for manipulating identity strings.
old-location: winauto\iaccpropservices.htm
old-project: WinAuto
ms.assetid: 0474dacf-7aa1-4d12-bac2-1091676a1ced
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IAccPropServices, IAccPropServices interface [Windows Accessibility], IAccPropServices interface [Windows Accessibility],described, msaa.iaccpropservices, oleacc/IAccPropServices, winauto.iaccpropservices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oleacc.h
api_name:
 - IAccPropServices
product: Windows
targetos: Windows
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAccPropServices interface


## -description


Exposes methods for annotating accessible elements and for manipulating identity strings. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccPropServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAccPropServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccPropServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fd3f595-4897-481f-972e-04cf1a4c6046">ClearHwndProps</a>
</td>
<td align="left" width="63%">
Restores default values to properties of <b>HWND</b>-based accessible elements that have been annotated previously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a3bce93-1d5d-48cf-84f4-cbca445b5451">ClearProps</a>
</td>
<td align="left" width="63%">
Restores default values to properties of accessible elements that have been annotated previously. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6712e47-7f00-4932-9a12-40ecafdbf584">ComposeHwndIdentityString</a>
</td>
<td align="left" width="63%">
Retrieves an identity string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b14932a1-7585-49e4-80eb-498cf48796ee">DecomposeHwndIdentityString</a>
</td>
<td align="left" width="63%">
Retrieves the <b>HWND</b>, object ID, and child ID for the accessible element identified by an identity string. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00387897-5385-467d-9da4-4d71fce742b6">SetHwndProp</a>
</td>
<td align="left" width="63%">
Sets a new value for a property on an <b>HWND</b>-based object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05dbdf97-9b1a-439f-b3a1-b517733ec0a8">SetHwndPropServer</a>
</td>
<td align="left" width="63%">
Specifies a callback object to be used to annotate an arrary of properties for an <b>HWND</b>-based accessible element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68f09a23-56b2-4fae-98a2-616b17fb4e1f">SetHwndPropStr</a>
</td>
<td align="left" width="63%">
Sets a new value for a string property on an <b>HWND</b>-based object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15e43a38-4cb3-43ca-a0fc-28faf49057dc">SetPropServer</a>
</td>
<td align="left" width="63%">
Specifies a callback object to be used to annotate an arrary of properties for the accessible element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c86acb70-fa77-4f95-8a99-e60872cdaa7e">SetPropValue</a>
</td>
<td align="left" width="63%">
Sets a new value for a property.

</td>
</tr>
</table> 

