---
UID: NN:radialcontrollerinterop.IRadialControllerConfigurationInterop
title: IRadialControllerConfigurationInterop
author: windows-sdk-content
description: Enables interoperability with a Universal Windows Platform (UWP)&#160;RadialControllerConfiguration object and provides access to RadialControllerConfiguration members for customizing a RadialController menu.
old-location: input_radial\iradialcontrollerconfigurationinterop.htm
old-project: Input_Radial
ms.assetid: eb8672c1-a7e6-45f5-a61f-3bee67f5ff5e
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IRadialControllerConfigurationInterop, IRadialControllerConfigurationInterop interface, IRadialControllerConfigurationInterop interface,described, Input_Radial.iradialcontrollerconfigurationinterop, radialcontrollerinterop/IRadialControllerConfigurationInterop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: RSVP_STATUS_INFO, *LPRSVP_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RadialControllerInterop.h
api_name:
 - IRadialControllerConfigurationInterop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IRadialControllerConfigurationInterop interface


## -description


Enables interoperability with a Universal Windows Platform (UWP) <a href="https://msdn.microsoft.com/f988ea33-43bf-4b0e-86bc-8ee56f41ed90">RadialControllerConfiguration</a> object and provides access to <b>RadialControllerConfiguration</b> members for customizing a <a href="https://msdn.microsoft.com/5cd9534d-bdd7-49fa-81c7-a5ddca4e851a">RadialController</a> menu.


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
<a href="https://msdn.microsoft.com/f2182f3a-82a8-40be-b331-673a181f4070">GetForWindow</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://msdn.microsoft.com/f988ea33-43bf-4b0e-86bc-8ee56f41ed90">RadialControllerConfiguration</a> object bound to the active application.

</td>
</tr>
</table> 


## -see-also




<b>Developer and UX guidance</b>



<a href="https://msdn.microsoft.com/44FED16E-63FB-466B-9615-8B744F861AE9">Radial controller interfaces</a>



<b>Samples</b>



<a href="https://go.microsoft.com/fwlink/?linkid=832322">Surface Dial interactions</a>



<a href="https://go.microsoft.com/fwlink/?linkid=832713">Universal Windows Platform samples (C# and C++)</a>



<a href="https://aka.ms/radialcontrollerclassicsample">Windows classic desktop sample</a>
 

 

