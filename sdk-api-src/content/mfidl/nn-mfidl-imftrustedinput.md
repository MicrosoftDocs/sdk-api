---
UID: NN:mfidl.IMFTrustedInput
title: IMFTrustedInput (mfidl.h)
description: Implemented by components that provide input trust authorities (ITAs). This interface is used to get the ITA for each of the component's streams.
helpviewer_keywords: ["59a9def7-69a6-4f80-bb5e-1cb372ff6eab","IMFTrustedInput","IMFTrustedInput interface [Media Foundation]","IMFTrustedInput interface [Media Foundation]","described","mf.imftrustedinput","mfidl/IMFTrustedInput"]
old-location: mf\imftrustedinput.htm
tech.root: mf
ms.assetid: 59a9def7-69a6-4f80-bb5e-1cb372ff6eab
ms.date: 12/05/2018
ms.keywords: 59a9def7-69a6-4f80-bb5e-1cb372ff6eab, IMFTrustedInput, IMFTrustedInput interface [Media Foundation], IMFTrustedInput interface [Media Foundation],described, mf.imftrustedinput, mfidl/IMFTrustedInput
f1_keywords:
- mfidl/IMFTrustedInput
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
- IMFTrustedInput
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTrustedInput interface


## -description


Implemented by components that provide input trust authorities (ITAs). This interface is used to get the ITA for each of the component's streams.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTrustedInput</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTrustedInput</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTrustedInput</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftrustedinput-getinputtrustauthority">GetInputTrustAuthority</a>
</td>
<td align="left" width="63%">
Retrieves the ITA for a specified stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

