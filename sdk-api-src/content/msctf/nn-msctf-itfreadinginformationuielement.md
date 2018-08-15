---
UID: NN:msctf.ITfReadingInformationUIElement
title: ITfReadingInformationUIElement
author: windows-sdk-content
description: The ITfCandidateListUIElement interface is implemented by a text service that has a UI for reading information UI at the near caret.
old-location: tsf\itfreadinginformationuielement.htm
old-project: TSF
ms.assetid: 60f7c6e2-7821-4be6-a1c1-35bacaa60bf4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfReadingInformationUIElement, ITfReadingInformationUIElement interface [Text Services Framework], ITfReadingInformationUIElement interface [Text Services Framework],described, msctf/ITfReadingInformationUIElement, tsf.itfreadinginformationuielement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfReadingInformationUIElement
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfReadingInformationUIElement interface


## -description


The <b>ITfCandidateListUIElement</b> interface is implemented by a text service that has a UI for reading information UI at the near caret.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfReadingInformationUIElement</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfReadingInformationUIElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfReadingInformationUIElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/018c10ca-698e-42e6-9439-09f183870f91">GetContext</a>
</td>
<td align="left" width="63%">
Returns the target ITfContext of this reading information UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c31bfbe7-c31a-485a-a122-14215d661ce7">GetErrorIndex</a>
</td>
<td align="left" width="63%">
Returns the char index where the typing error occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a26aa8d0-a447-4ebb-b892-28b959b57681">GetMaxReadingStringLength</a>
</td>
<td align="left" width="63%">
Returns the max string count of the reading information UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8e7dae5-ea73-4fad-a731-3ca1eaa60b03">GetString</a>
</td>
<td align="left" width="63%">
Returns the string on the reading information UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a5b1a50-9d0b-440a-a98f-80fd33c6cd95">GetUpdatedFlags</a>
</td>
<td align="left" width="63%">
Returns the flag that tells which part of this element was updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a45d8928-5cfd-4af9-ba3b-7171e48d81c8">IsVerticalOrderPreferred</a>
</td>
<td align="left" width="63%">
Returns if the UI prefers to be shown in vertical order.

</td>
</tr>
</table> 

