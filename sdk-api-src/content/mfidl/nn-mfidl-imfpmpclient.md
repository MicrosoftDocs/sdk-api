---
UID: NN:mfidl.IMFPMPClient
title: IMFPMPClient (mfidl.h)
description: Enables a media source to receive a pointer to the IMFPMPHost interface.
helpviewer_keywords: ["IMFPMPClient","IMFPMPClient interface [Media Foundation]","IMFPMPClient interface [Media Foundation]","described","adfba5dd-eae6-48f3-a155-65bd491c952c","mf.imfpmpclient","mfidl/IMFPMPClient"]
old-location: mf\imfpmpclient.htm
tech.root: mf
ms.assetid: adfba5dd-eae6-48f3-a155-65bd491c952c
ms.date: 12/05/2018
ms.keywords: IMFPMPClient, IMFPMPClient interface [Media Foundation], IMFPMPClient interface [Media Foundation],described, adfba5dd-eae6-48f3-a155-65bd491c952c, mf.imfpmpclient, mfidl/IMFPMPClient
f1_keywords:
- mfidl/IMFPMPClient
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
- IMFPMPClient
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMPClient interface


## -description


Enables a media source to receive a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmphost">IMFPMPHost</a> interface.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMPClient</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMPClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMPClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost">SetPMPHost</a>
</td>
<td align="left" width="63%">
Provides a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmphost">IMFPMPHost</a> interface.
        

</td>
</tr>
</table> 


## -remarks



If a media source exposes this interface, the Protected Media Path (PMP) Media Session calls <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost">SetPMPHost</a> with a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmphost">IMFPMPHost</a> interface. The media source can use the <b>IMFPMPHost</b> interface to create objects in the PMP process.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
 

 

