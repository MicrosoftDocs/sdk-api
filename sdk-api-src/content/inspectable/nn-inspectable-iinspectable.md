---
UID: NN:inspectable.IInspectable
title: IInspectable (inspectable.h)
description: Provides functionality required for all Windows Runtime classes.
helpviewer_keywords: ["IInspectable","IInspectable interface [Windows Runtime]","IInspectable interface [Windows Runtime]","described","inspectable/IInspectable","winrt.iinspectable"]
old-location: winrt\iinspectable.htm
tech.root: WinRT
ms.assetid: 0657E51F-D4C0-46C6-927D-B01E54B6846C
ms.date: 12/05/2018
ms.keywords: IInspectable, IInspectable interface [Windows Runtime], IInspectable interface [Windows Runtime],described, inspectable/IInspectable, winrt.iinspectable
f1_keywords:
- inspectable/IInspectable
dev_langs:
- c++
req.header: inspectable.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inspectable.idl
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
- Inspectable.h
api_name:
- IInspectable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInspectable interface


## -description


Provides functionality required for all Windows Runtime classes.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInspectable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInspectable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInspectable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nf-inspectable-iinspectable-getiids">GetIids</a>
</td>
<td align="left" width="63%">
Gets the interfaces that are implemented by the current Windows Runtime class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nf-inspectable-iinspectable-getruntimeclassname">GetRuntimeClassName</a>
</td>
<td align="left" width="63%">
Gets the fully qualified name of the current Windows Runtime object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nf-inspectable-iinspectable-gettrustlevel">GetTrustLevel</a>
</td>
<td align="left" width="63%">
Gets the trust level of the current Windows Runtime object.

</td>
</tr>
</table> 


## -remarks



<b>IInspectable</b> methods have no effect on COM apartments and are safe to call from user interface threads.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/ne-inspectable-trustlevel">TrustLevel</a>
 

 

