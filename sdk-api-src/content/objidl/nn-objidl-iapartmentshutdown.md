---
UID: NN:objidl.IApartmentShutdown
title: IApartmentShutdown (objidl.h)
description: Enables registration of an apartment shutdown notification handler.helpviewer_keywords: ["IApartmentShutdown","IApartmentShutdown interface [Windows Runtime]","IApartmentShutdown interface [Windows Runtime]","described","objidl/IApartmentShutdown","winrt.iapartmentshutdown"]
old-location: winrt\iapartmentshutdown.htm
tech.root: WinRT
ms.assetid: 28EDAC77-5175-4AF7-A06C-B735336AAD9B
ms.date: 12/05/2018
ms.keywords: IApartmentShutdown, IApartmentShutdown interface [Windows Runtime], IApartmentShutdown interface [Windows Runtime],described, objidl/IApartmentShutdown, winrt.iapartmentshutdown
f1_keywords:
- objidl/IApartmentShutdown
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
- objidl.h
api_name:
- IApartmentShutdown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IApartmentShutdown interface


## -description


Enables registration of  an apartment shutdown notification handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IApartmentShutdown</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IApartmentShutdown</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IApartmentShutdown</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iapartmentshutdown-onuninitialize">OnUninitialize</a>
</td>
<td align="left" width="63%">
Called when a registered apartment is shut down.

</td>
</tr>
</table> 


## -remarks



Implement the <b>IApartmentShutdown</b> interface to use the <a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-roregisterforapartmentshutdown">RoRegisterForApartmentShutdown</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-roregisterforapartmentshutdown">RoRegisterForApartmentShutdown</a>
 

 

