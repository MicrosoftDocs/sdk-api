---
UID: NN:mfidl.IMFSAMIStyle
title: IMFSAMIStyle (mfidl.h)
description: Sets and retrieves Synchronized Accessible Media Interchange (SAMI) styles on the SAMI Media Source.
helpviewer_keywords: ["IMFSAMIStyle","IMFSAMIStyle interface [Media Foundation]","IMFSAMIStyle interface [Media Foundation]","described","c4887c52-57af-4783-b853-11fe6ad3510e","mf.imfsamistyle","mfidl/IMFSAMIStyle"]
old-location: mf\imfsamistyle.htm
tech.root: mf
ms.assetid: c4887c52-57af-4783-b853-11fe6ad3510e
ms.date: 12/05/2018
ms.keywords: IMFSAMIStyle, IMFSAMIStyle interface [Media Foundation], IMFSAMIStyle interface [Media Foundation],described, c4887c52-57af-4783-b853-11fe6ad3510e, mf.imfsamistyle, mfidl/IMFSAMIStyle
f1_keywords:
- mfidl/IMFSAMIStyle
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFSAMIStyle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSAMIStyle interface


## -description


Sets and retrieves Synchronized Accessible Media Interchange (SAMI) styles on the <a href="https://docs.microsoft.com/windows/desktop/medfound/sami-media-source">SAMI Media Source</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSAMIStyle</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSAMIStyle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSAMIStyle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getselectedstyle">GetSelectedStyle</a>
</td>
<td align="left" width="63%">
Gets the current style from the SAMI media source.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount">GetStyleCount</a>
</td>
<td align="left" width="63%">
Gets the number of styles defined in the SAMI file.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles">GetStyles</a>
</td>
<td align="left" width="63%">
Gets a list of the style names defined in the SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle">SetSelectedStyle</a>
</td>
<td align="left" width="63%">
Sets the current style on the SAMI media source.
        

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier is <b>MF_SAMI_SERVICE</b>. Call <b>GetService</b> either directly on the SAMI media source, or on the Media Session (if you are using the SAMI source with the Media Session).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/sami-media-source">SAMI Media Source</a>
 

 

