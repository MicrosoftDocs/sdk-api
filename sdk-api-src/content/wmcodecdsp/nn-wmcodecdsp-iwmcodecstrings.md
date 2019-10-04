---
UID: NN:wmcodecdsp.IWMCodecStrings
title: IWMCodecStrings (wmcodecdsp.h)
author: windows-sdk-content
description: Retrieves names and descriptive strings for codecs and formats.
old-location: mf\iwmcodecstringsinterface.htm
tech.root: medfound
ms.assetid: 84b6223e-d42a-47b0-8553-2b4d69de2da3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMCodecStrings, IWMCodecStrings interface [Media Foundation], IWMCodecStrings interface [Media Foundation],described, codecapi.iwmcodecstringsinterface, mf.iwmcodecstringsinterface, wmcodecdsp/IWMCodecStrings
ms.topic: interface
f1_keywords: 
 - "wmcodecdsp/IWMCodecStrings"
dev_langs:
 - c++
req.header: wmcodecdsp.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMCodecStrings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMCodecStrings interface


## -description


Retrieves names and descriptive strings for codecs and formats.

This interface is implemented by all of the codec encoder objects. You can retrieve a pointer to the <b>IWMCodecStrings</b> interface for any encoder by calling the <b>QueryInterface</b> method of any other interface on the object, such as <a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>, This interface is not implemented on any of the decoder DMOs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecStrings</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCodecStrings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecStrings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecstrings-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of an output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecstrings-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a codec.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

