---
UID: NN:tuner.ITunerCap
title: ITunerCap (tuner.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005. The ITunerCap interface provides information about the capabilities of a BDA device filter that represents a TV tuner.helpviewer_keywords: ["ITunerCap","ITunerCap interface [Microsoft TV Technologies]","ITunerCap interface [Microsoft TV Technologies]","described","ITunerCapInterface","mstv.itunercap","tuner/ITunerCap"]
old-location: mstv\itunercap.htm
tech.root: mstv
ms.assetid: d7027ff4-4fb9-48c1-b527-92e65009b089
ms.date: 12/05/2018
ms.keywords: ITunerCap, ITunerCap interface [Microsoft TV Technologies], ITunerCap interface [Microsoft TV Technologies],described, ITunerCapInterface, mstv.itunercap, tuner/ITunerCap
f1_keywords:
- tuner/ITunerCap
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tuner.h
api_name:
- ITunerCap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITunerCap interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>ITunerCap</b> interface provides information about the capabilities of a BDA device filter that represents a TV tuner.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITunerCap</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITunerCap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITunerCap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-itunercap-get_auxinputcount">get_AuxInputCount</a>
</td>
<td align="left" width="63%">
Retrieves a count of the number of auxiliary inputs on the TV tuner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-itunercap-get_supportednetworktypes">get_SupportedNetworkTypes</a>
</td>
<td align="left" width="63%">
Retrieves a list of the network types that are supported by the TV tuner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-itunercap-get_supportedvideoformats">get_SupportedVideoFormats</a>
</td>
<td align="left" width="63%">
Retrieves the video formats that are supported by the TV tuner.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITunerCap)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

