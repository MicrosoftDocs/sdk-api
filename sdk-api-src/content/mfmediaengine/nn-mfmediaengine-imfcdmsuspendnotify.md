---
UID: NN:mfmediaengine.IMFCdmSuspendNotify
title: IMFCdmSuspendNotify (mfmediaengine.h)
author: windows-sdk-content
description: Used to enable the client to notify the Content Decryption Module (CDM) when global resources should be brought into a consistent state prior to suspending.
old-location: mf\imfcdmsuspendnotify.htm
tech.root: medfound
ms.assetid: b2671b66-fa9e-46a4-887e-d3ba9dd9025b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFCdmSuspendNotify, IMFCdmSuspendNotify interface [Media Foundation], IMFCdmSuspendNotify interface [Media Foundation],described, mf.imfcdmsuspendnotify, mfmediaengine/IMFCdmSuspendNotify
ms.topic: interface
f1_keywords: 
 - "mfmediaengine/IMFCdmSuspendNotify"
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFCdmSuspendNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCdmSuspendNotify interface


## -description


Used to enable the client to notify the Content Decryption Module (CDM) when global resources should be brought into a consistent state prior to suspending.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCdmSuspendNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFCdmSuspendNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCdmSuspendNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfcdmsuspendnotify-begin">Begin</a>
</td>
<td align="left" width="63%">
Indicates that the suspend process is starting and  resources should be brought into a consistent state.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfcdmsuspendnotify-end">End</a>
</td>
<td align="left" width="63%">
The actual suspend is about to occur and no more calls will be made into the Content Decryption Module (CDM).

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

