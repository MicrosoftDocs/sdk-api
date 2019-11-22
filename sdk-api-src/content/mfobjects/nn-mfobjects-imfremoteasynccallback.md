---
UID: NN:mfobjects.IMFRemoteAsyncCallback
title: IMFRemoteAsyncCallback (mfobjects.h)

description: Used by the Microsoft Media Foundation proxy/stub DLL to marshal certain asynchronous method calls across process boundaries.Applications do not use or implement this interface.
old-location: mf\imfremoteasynccallback.htm
tech.root: medfound
ms.assetid: 57be21cf-b381-436a-bc7e-3fdc01cc2515

ms.date: 12/05/2018
ms.keywords: 57be21cf-b381-436a-bc7e-3fdc01cc2515, IMFRemoteAsyncCallback, IMFRemoteAsyncCallback interface [Media Foundation], IMFRemoteAsyncCallback interface [Media Foundation],described, mf.imfremoteasynccallback, mfobjects/IMFRemoteAsyncCallback
ms.topic: interface
f1_keywords: 
 - "mfobjects/IMFRemoteAsyncCallback"
dev_langs:
 - c++
req.header: mfobjects.h
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
 - IMFRemoteAsyncCallback
 - IMFRemoteAsyncCallback.Invoke
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFRemoteAsyncCallback interface


## -description



Used by the Microsoft Media Foundation proxy/stub DLL to marshal certain asynchronous method calls across process boundaries.

Applications do not use or implement this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFRemoteAsyncCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFRemoteAsyncCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFRemoteAsyncCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>Invoke</b></td>
<td align="left" width="63%">
Not used by applications.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

