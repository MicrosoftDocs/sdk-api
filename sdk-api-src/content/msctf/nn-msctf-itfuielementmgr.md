---
UID: NN:msctf.ITfUIElementMgr
title: ITfUIElementMgr
author: windows-driver-content
description: The ITfUIElementMgr interface is implemented by TSF manager and used by an application or a text service. An application and a text service can obtain this interface by ITfThreadMgr::QueryInterface with IID_ITfUIElementMgr.
old-location: tsf\itfuielementmgr.htm
old-project: TSF
ms.assetid: 7b4d3f4e-bf30-45c6-8709-88b71b25d333
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfUIElementMgr, ITfUIElementMgr interface [Text Services Framework], ITfUIElementMgr interface [Text Services Framework],described, _tsf_itfuielementmgr_ref, msctf/ITfUIElementMgr, tsf.itfuielementmgr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.h
api_name:
-	ITfUIElementMgr
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfUIElementMgr interface


## -description


The <b>ITfUIElementMgr</b> interface is implemented by TSF manager and used by an application or a text service. An application and a text service can obtain this interface by ITfThreadMgr::QueryInterface with IID_ITfUIElementMgr.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfUIElementMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfUIElementMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfUIElementMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c522920-8bd7-4385-b77d-34df26967179">BeginUIElement</a>
</td>
<td align="left" width="63%">
A text service calls this method before showing UI. It returns if the text service’s UI should be shown or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cec22994-c233-4f84-8237-749ef3cc8aff">EndUIElement</a>
</td>
<td align="left" width="63%">
A text service calls this method when the element of UI is hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdede376-be18-4deb-ae79-594aebb085a6">EnumUIElements</a>
</td>
<td align="left" width="63%">
Return IEnumTfUIElements interface poinssster to enumerate the ITfUIElement.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3a2a7ae-1ca2-4c1e-83af-207821966147">GetUIElement</a>
</td>
<td align="left" width="63%">
Get ITfUIElement interface of the element id.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7df9abf-53a0-41a4-aac5-d90b9abfbeec">UpdateUIElement</a>
</td>
<td align="left" width="63%">
A text service calls this method when the element of UI must be updated.

</td>
</tr>
</table> 


## -remarks



A text service that supports UIElement must call <b>ITfUIElementMgr</b> whenever the UI is shown, updated or hidden. Then the application can control the visibility of the UI.



