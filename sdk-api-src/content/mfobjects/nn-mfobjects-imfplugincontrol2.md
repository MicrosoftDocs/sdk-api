---
UID: NN:mfobjects.IMFPluginControl2
title: IMFPluginControl2 (mfobjects.h)
description: Controls how media sources and transforms are enumerated in Microsoft Media Foundation.
helpviewer_keywords: ["IMFPluginControl2","IMFPluginControl2 interface [Media Foundation]","IMFPluginControl2 interface [Media Foundation]","described","mf.imfplugincontrol2","mfobjects/IMFPluginControl2"]
old-location: mf\imfplugincontrol2.htm
tech.root: mf
ms.assetid: 15BD57FC-7CEF-45DC-AF94-3E54A3A9477A
ms.date: 12/05/2018
ms.keywords: IMFPluginControl2, IMFPluginControl2 interface [Media Foundation], IMFPluginControl2 interface [Media Foundation],described, mf.imfplugincontrol2, mfobjects/IMFPluginControl2
f1_keywords:
- mfobjects/IMFPluginControl2
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- mfobjects.h
api_name:
- IMFPluginControl2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPluginControl2 interface


## -description


Controls how media sources and transforms are enumerated in Microsoft Media Foundation.

This interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPluginControl2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>. <b>IMFPluginControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPluginControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol2-setpolicy">SetPolicy</a>
</td>
<td align="left" width="63%">
Sets the policy for which media sources and transforms are enumerated.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfgetplugincontrol">MFGetPluginControl</a>  and query the returned pointer for <b>IMFPluginControl2</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

