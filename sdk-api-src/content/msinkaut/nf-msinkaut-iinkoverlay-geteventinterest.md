---
UID: NF:msinkaut.IInkOverlay.GetEventInterest
title: IInkOverlay::GetEventInterest (msinkaut.h)
description: Retrieves the interest an object has in a particular event for the InkCollector class, InkOverlay class, or InkPicture class. (IInkOverlay.GetEventInterest)
helpviewer_keywords: ["532a798e-b434-4730-8c20-7ec60255f170","GetEventInterest","GetEventInterest method [Tablet PC]","GetEventInterest method [Tablet PC]","IInkOverlay interface","IInkOverlay interface [Tablet PC]","GetEventInterest method","IInkOverlay.GetEventInterest","IInkOverlay::GetEventInterest","msinkaut/IInkOverlay::GetEventInterest","tablet.inkoverlay_geteventinterest"]
old-location: tablet\inkoverlay_geteventinterest.htm
tech.root: tablet
ms.assetid: 709ba46e-fc39-4b91-b145-72381a1195a1
ms.date: 12/05/2018
ms.keywords: 532a798e-b434-4730-8c20-7ec60255f170, GetEventInterest, GetEventInterest method [Tablet PC], GetEventInterest method [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],GetEventInterest method, IInkOverlay.GetEventInterest, IInkOverlay::GetEventInterest, msinkaut/IInkOverlay::GetEventInterest, tablet.inkoverlay_geteventinterest
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
 - IInkOverlay::GetEventInterest
 - msinkaut/IInkOverlay::GetEventInterest
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
 - IInkOverlay.GetEventInterest
---

# IInkOverlay::GetEventInterest


## -description

Retrieves the interest an object has in a particular event for the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> class, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> class, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> class.

## -parameters

### -param EventId [in]

The event in which the ink collector is or is not interested.

### -param Listen [out, retval]

<b>VARIANT_TRUE</b> if interest in the specified event has been set; otherwise, <b>VARIANT_FALSE</b>.

## -returns

This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid event interest.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred during processing.

</td>
</tr>
</table>

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectoreventinterest">InkCollectorEventInterest Enumeration</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest">SetEventInterest Method</a>
