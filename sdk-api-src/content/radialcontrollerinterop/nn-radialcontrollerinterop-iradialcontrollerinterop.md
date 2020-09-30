---
UID: NN:radialcontrollerinterop.IRadialControllerInterop
title: IRadialControllerInterop (radialcontrollerinterop.h)
description: Enables interoperability with a Universal Windows Platform (UWP)�RadialController object and provides access to RadialController members for customizing the interaction experience.
helpviewer_keywords: ["IRadialControllerInterop","IRadialControllerInterop interface","IRadialControllerInterop interface","described","Input_Radial.iradialcontrollerinterop","radialcontrollerinterop/IRadialControllerInterop"]
old-location: input_radial\iradialcontrollerinterop.htm
tech.root: input_radial
ms.assetid: ed701930-fae7-4c42-9e6b-b1cb3fac861c
ms.date: 12/05/2018
ms.keywords: IRadialControllerInterop, IRadialControllerInterop interface, IRadialControllerInterop interface,described, Input_Radial.iradialcontrollerinterop, radialcontrollerinterop/IRadialControllerInterop
req.header: radialcontrollerinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RadialControllerInterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRadialControllerInterop
 - radialcontrollerinterop/IRadialControllerInterop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RadialControllerInterop.h
api_name:
 - IRadialControllerInterop
---

# IRadialControllerInterop interface


## -description

Enables interoperability with a Universal Windows Platform (UWP) <a href="/uwp/api/windows.ui.input.radialcontroller">RadialController</a> object and provides access to <b>RadialController</b> members for customizing the interaction experience.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRadialControllerInterop</b> interface inherits from <b>IInspectable</b>. <b>IRadialControllerInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRadialControllerInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/radialcontrollerinterop/nf-radialcontrollerinterop-iradialcontrollerinterop-createforwindow">CreateForWindow</a>
</td>
<td align="left" width="63%">
Instantiates a <a href="/uwp/api/windows.ui.input.radialcontroller">RadialController</a> object and binds it to the active application.

</td>
</tr>
</table>

## -see-also

<b>Developer and UX guidance</b>



<a href="/previous-versions/windows/desktop/input_radial/radial-controller-interfaces">Radial controller interfaces</a>



<b>Samples</b>



<a href="/windows/uwp/design/input/windows-wheel-interactions">Surface Dial interactions</a>



<a href="https://github.com/Microsoft/Windows-universal-samples/tree/b78d95134ce2d57c848e0a8dc339fc362748fb9c/Samples/RadialController">Universal Windows Platform samples (C# and C++)</a>



<a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/RadialController">Windows classic desktop sample</a>