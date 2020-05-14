---
UID: NN:mfidl.IMFSourceOpenMonitor
title: IMFSourceOpenMonitor (mfidl.h)
description: Callback interface to receive notifications from a network source on the progress of an asynchronous open operation.helpviewer_keywords: ["9145910b-81f1-4fd1-8f6f-d6273e0edde6","IMFSourceOpenMonitor","IMFSourceOpenMonitor interface [Media Foundation]","IMFSourceOpenMonitor interface [Media Foundation]","described","mf.imfsourceopenmonitor","mfidl/IMFSourceOpenMonitor"]
old-location: mf\imfsourceopenmonitor.htm
tech.root: medfound
ms.assetid: 9145910b-81f1-4fd1-8f6f-d6273e0edde6
ms.date: 12/05/2018
ms.keywords: 9145910b-81f1-4fd1-8f6f-d6273e0edde6, IMFSourceOpenMonitor, IMFSourceOpenMonitor interface [Media Foundation], IMFSourceOpenMonitor interface [Media Foundation],described, mf.imfsourceopenmonitor, mfidl/IMFSourceOpenMonitor
f1_keywords:
- mfidl/IMFSourceOpenMonitor
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
- IMFSourceOpenMonitor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSourceOpenMonitor interface


## -description


Callback interface to receive notifications from a network source on the progress of an asynchronous open operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceOpenMonitor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceOpenMonitor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceOpenMonitor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent">OnSourceEvent</a>
</td>
<td align="left" width="63%">
Called by the network source when the open operation begins or ends.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-get-events-from-the-network-source">How to Get Events from the Network Source</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

