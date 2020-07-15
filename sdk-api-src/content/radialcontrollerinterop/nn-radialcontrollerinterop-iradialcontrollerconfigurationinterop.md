---
UID: NN:radialcontrollerinterop.IRadialControllerConfigurationInterop
title: IRadialControllerConfigurationInterop (radialcontrollerinterop.h)
description: Enables interoperability with a Universal Windows Platform (UWP)�RadialControllerConfiguration object and provides access to RadialControllerConfiguration members for customizing a RadialController menu.
helpviewer_keywords: ["IRadialControllerConfigurationInterop","IRadialControllerConfigurationInterop interface","IRadialControllerConfigurationInterop interface","described","Input_Radial.iradialcontrollerconfigurationinterop","radialcontrollerinterop/IRadialControllerConfigurationInterop"]
old-location: input_radial\iradialcontrollerconfigurationinterop.htm
tech.root: Input_Radial
ms.assetid: eb8672c1-a7e6-45f5-a61f-3bee67f5ff5e
ms.date: 12/05/2018
ms.keywords: IRadialControllerConfigurationInterop, IRadialControllerConfigurationInterop interface, IRadialControllerConfigurationInterop interface,described, Input_Radial.iradialcontrollerconfigurationinterop, radialcontrollerinterop/IRadialControllerConfigurationInterop
f1_keywords:
- radialcontrollerinterop/IRadialControllerConfigurationInterop
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- RadialControllerInterop.h
api_name:
- IRadialControllerConfigurationInterop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRadialControllerConfigurationInterop interface


## -description


Enables interoperability with a Universal Windows Platform (UWP) <a href="https://docs.microsoft.com/uwp/api/windows.ui.input.radialcontrollerconfiguration">RadialControllerConfiguration</a> object and provides access to <b>RadialControllerConfiguration</b> members for customizing a <a href="https://docs.microsoft.com/uwp/api/windows.ui.input.radialcontroller">RadialController</a> menu.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRadialControllerConfigurationInterop</b> interface inherits from <b>IInspectable</b>. <b>IRadialControllerConfigurationInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRadialControllerConfigurationInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/radialcontrollerinterop/nf-radialcontrollerinterop-iradialcontrollerconfigurationinterop-getforwindow">GetForWindow</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://docs.microsoft.com/uwp/api/windows.ui.input.radialcontrollerconfiguration">RadialControllerConfiguration</a> object bound to the active application.

</td>
</tr>
</table> 


## -see-also




<b>Developer and UX guidance</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_radial/radial-controller-interfaces">Radial controller interfaces</a>



<b>Samples</b>



<a href="https://docs.microsoft.com/windows/uwp/design/input/windows-wheel-interactions?redirectedfrom=MSDN">Surface Dial interactions</a>



<a href="https://github.com/Microsoft/Windows-universal-samples/tree/b78d95134ce2d57c848e0a8dc339fc362748fb9c/Samples/RadialController">Universal Windows Platform samples (C# and C++)</a>



<a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/RadialController">Windows classic desktop sample</a>
 

 

