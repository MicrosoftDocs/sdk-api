---
UID: NN:msinkaut.IInkLineInfo
title: IInkLineInfo (msinkaut.h)
description: The IInkLineInfo interface provides access to the display properties and recognition result list of a text ink object (tInk).
helpviewer_keywords: ["58774f49-6af2-4b81-bbd5-709eb694af2d","IInkLineInfo","IInkLineInfo interface [Tablet PC]","IInkLineInfo interface [Tablet PC]","described","msinkaut/IInkLineInfo","tablet.iinklineinfo"]
old-location: tablet\iinklineinfo.htm
tech.root: tablet
ms.assetid: 58774f49-6af2-4b81-bbd5-709eb694af2d
ms.date: 12/05/2018
ms.keywords: 58774f49-6af2-4b81-bbd5-709eb694af2d, IInkLineInfo, IInkLineInfo interface [Tablet PC], IInkLineInfo interface [Tablet PC],described, msinkaut/IInkLineInfo, tablet.iinklineinfo
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkLineInfo
 - msinkaut/IInkLineInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkLineInfo
---

# IInkLineInfo interface


## -description

The <b>IInkLineInfo</b> interface provides access to the display properties and recognition result list of a text ink object (tInk).

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkLineInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkLineInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInkLineInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getcandidate">GetCandidate</a>
</td>
<td align="left" width="63%">
Returns one word from the recognition alternates list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getformat">GetFormat</a>
</td>
<td align="left" width="63%">
Returns the display properties currently set on the text ink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent">GetInkExtent</a>
</td>
<td align="left" width="63%">
Specifies the display properties to set on the text ink object, and retrieves the width of the text ink object in <b>HIMETRIC</b> units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-recognize">Recognize</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-setcandidate">SetCandidate</a>
</td>
<td align="left" width="63%">
Updates one recognition alternate in the recognition result list, either by replacing an existing alternate, or by adding an alternate to the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-setformat">SetFormat</a>
</td>
<td align="left" width="63%">
Specifies the display properties to set on the text ink object.

</td>
</tr>
</table>

