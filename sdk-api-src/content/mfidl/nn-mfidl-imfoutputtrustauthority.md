---
UID: NN:mfidl.IMFOutputTrustAuthority
title: IMFOutputTrustAuthority (mfidl.h)
description: Encapsulates the functionality of one or more output protection systems that a trusted output supports.
old-location: mf\imfoutputtrustauthority.htm
tech.root: medfound
ms.assetid: 21594ac0-7e3c-44a3-bbee-64316dd51824
ms.date: 12/05/2018
ms.keywords: 21594ac0-7e3c-44a3-bbee-64316dd51824, IMFOutputTrustAuthority, IMFOutputTrustAuthority interface [Media Foundation], IMFOutputTrustAuthority interface [Media Foundation],described, mf.imfoutputtrustauthority, mfidl/IMFOutputTrustAuthority
ms.topic: interface
f1_keywords:
- mfidl/IMFOutputTrustAuthority
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
- IMFOutputTrustAuthority
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFOutputTrustAuthority interface


## -description


Encapsulates the functionality of one or more output protection systems that a trusted output supports. This interface is exposed by output trust authority (OTA) objects. Each OTA represents a single action that the trusted output can perform, such as play, copy, or transcode. An OTA can represent more than one physical output if each output performs the same action.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFOutputTrustAuthority</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFOutputTrustAuthority</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFOutputTrustAuthority</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-getaction">GetAction</a>
</td>
<td align="left" width="63%">
Retrieves the action that is performed by this OTA.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy">SetPolicy</a>
</td>
<td align="left" width="63%">
Sets one or more policy objects on the OTA.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

