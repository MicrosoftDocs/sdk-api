---
UID: NN:mfidl.IMFQualityAdviseLimits
title: IMFQualityAdviseLimits (mfidl.h)
description: Queries an object for the number of quality modes it supports.
helpviewer_keywords: ["IMFQualityAdviseLimits","IMFQualityAdviseLimits interface [Media Foundation]","IMFQualityAdviseLimits interface [Media Foundation]","described","mf.imfqualityadviselimits","mfidl/IMFQualityAdviseLimits"]
old-location: mf\imfqualityadviselimits.htm
tech.root: medfound
ms.assetid: 8ef7088c-2f49-4be9-b719-481616e1737d
ms.date: 12/05/2018
ms.keywords: IMFQualityAdviseLimits, IMFQualityAdviseLimits interface [Media Foundation], IMFQualityAdviseLimits interface [Media Foundation],described, mf.imfqualityadviselimits, mfidl/IMFQualityAdviseLimits
f1_keywords:
- mfidl/IMFQualityAdviseLimits
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfidl.h
api_name:
- IMFQualityAdviseLimits
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFQualityAdviseLimits interface


## -description


Queries an object for the number of <i>quality modes</i> it supports. Quality modes are used to adjust the trade-off between quality and speed when rendering audio or video.

The default presenter for the <i>enhanced video renderer</i> (EVR) implements this interface. The EVR uses the interface to respond to quality messages from the quality manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFQualityAdviseLimits</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFQualityAdviseLimits</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFQualityAdviseLimits</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualityadviselimits-getmaximumdropmode">GetMaximumDropMode</a>
</td>
<td align="left" width="63%">
Gets the maximum drop mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualityadviselimits-getminimumqualitylevel">GetMinimumQualityLevel</a>
</td>
<td align="left" width="63%">
Gets the minimum quality level that is  supported by the component.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

