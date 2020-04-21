---
UID: NN:mfidl.IMFGetService
title: IMFGetService (mfidl.h)
description: Queries an object for a specified service interface.helpviewer_keywords: ["102a1dff-8419-4f86-a145-53ce3d0123f5","IMFGetService","IMFGetService interface [Media Foundation]","IMFGetService interface [Media Foundation]","described","mf.imfgetservice","mfidl/IMFGetService"]
old-location: mf\imfgetservice.htm
tech.root: medfound
ms.assetid: 102a1dff-8419-4f86-a145-53ce3d0123f5
ms.date: 12/05/2018
ms.keywords: 102a1dff-8419-4f86-a145-53ce3d0123f5, IMFGetService, IMFGetService interface [Media Foundation], IMFGetService interface [Media Foundation],described, mf.imfgetservice, mfidl/IMFGetService
f1_keywords:
- mfidl/IMFGetService
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
- IMFGetService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFGetService interface


## -description


Queries an object for a specified service interface.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFGetService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFGetService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFGetService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">GetService</a>
</td>
<td align="left" width="63%">
Retrieves a service interface.

</td>
</tr>
</table> 


## -remarks



A service is an interface that is exposed by one object but might be implemented by another object. The <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">GetService</a> method is equivalent to <b>QueryInterface</b>, with the following difference: when <b>QueryInterface</b> retrieves a pointer to an interface, it is guaranteed that you can query the returned interface and get back the original interface. The <b>GetService</b> method does not make this guarantee, because the retrieved interface might be implemented by a separate object.

The <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfgetservice">MFGetService</a> function is a helper function that queries an object for <b>IMFGetService</b> and calls the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">GetService</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/service-interfaces">Service Interfaces</a>
 

 

