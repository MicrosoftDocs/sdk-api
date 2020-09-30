---
UID: NN:tuner.IMPEG2ComponentType
title: IMPEG2ComponentType (tuner.h)
description: The IMPEG2ComponentType interface is implemented on MPEG2ComponentType objects. It enables applications to set and retrieve information about MPEG2 stream types.
helpviewer_keywords: ["IMPEG2ComponentType","IMPEG2ComponentType interface [Microsoft TV Technologies]","IMPEG2ComponentType interface [Microsoft TV Technologies]","described","IMPEG2ComponentTypeInterface","mstv.impeg2componenttype","tuner/IMPEG2ComponentType"]
old-location: mstv\impeg2componenttype.htm
tech.root: mstv
ms.assetid: 10bf35e0-d5bf-41ed-b514-7c1bfaf774a0
ms.date: 12/05/2018
ms.keywords: IMPEG2ComponentType, IMPEG2ComponentType interface [Microsoft TV Technologies], IMPEG2ComponentType interface [Microsoft TV Technologies],described, IMPEG2ComponentTypeInterface, mstv.impeg2componenttype, tuner/IMPEG2ComponentType
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMPEG2ComponentType
 - tuner/IMPEG2ComponentType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IMPEG2ComponentType
---

# IMPEG2ComponentType interface


## -description

The <b>IMPEG2ComponentType</b> interface is implemented on <a href="/previous-versions/windows/desktop/mstv/mpeg2componenttype-object">MPEG2ComponentType</a> objects. It enables applications to set and retrieve information about MPEG2 stream types.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2ComponentType</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilanguagecomponenttype">ILanguageComponentType</a>. <b>IMPEG2ComponentType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2ComponentType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2componenttype-get_streamtype">get_StreamType</a>
</td>
<td align="left" width="63%">
Retrieves the stream type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-impeg2componenttype-put_streamtype">put_StreamType</a>
</td>
<td align="left" width="63%">
Sets the stream type.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2ComponentType)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilanguagecomponenttype">ILanguageComponentType</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>