---
UID: NN:activationregistration.IActivatableClassRegistration
title: IActivatableClassRegistration (activationregistration.h)
description: Enables getting the registration info for a class.
helpviewer_keywords: ["IActivatableClassRegistration","IActivatableClassRegistration interface [Windows Runtime]","IActivatableClassRegistration interface [Windows Runtime]","described","activationregistration/IActivatableClassRegistration","winrt.iactivatableclassregistration"]
old-location: winrt\iactivatableclassregistration.htm
tech.root: WinRT
ms.assetid: 99834A2D-547B-4B04-8703-46B11E0BB812
ms.date: 12/05/2018
ms.keywords: IActivatableClassRegistration, IActivatableClassRegistration interface [Windows Runtime], IActivatableClassRegistration interface [Windows Runtime],described, activationregistration/IActivatableClassRegistration, winrt.iactivatableclassregistration
req.header: activationregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActivatableClassRegistration
 - activationregistration/IActivatableClassRegistration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - activationregistration.h
api_name:
 - IActivatableClassRegistration
---

# IActivatableClassRegistration interface


## -description

Enables getting  the registration info for a class.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActivatableClassRegistration</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IActivatableClassRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActivatableClassRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iactivatableclassregistration-get_activatableclassid">get_ActivatableClassId</a>
</td>
<td align="left" width="63%">
Gets the class identifier for the current activatable class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iactivatableclassregistration-get_activationtype">get_ActivationType</a>
</td>
<td align="left" width="63%">
Gets the kind of activation for the current activatable class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iactivatableclassregistration-get_attributes">get_Attributes</a>
</td>
<td align="left" width="63%">
Gets the attributes associated with the current activatable class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iactivatableclassregistration-get_registeredtrustlevel">get_RegisteredTrustLevel</a>
</td>
<td align="left" width="63%">
Gets the trust level of the current activatable class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-iactivatableclassregistration-get_registrationscope">get_RegistrationScope</a>
</td>
<td align="left" width="63%">
Gets the deployment scope of the current activatable class.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nn-activationregistration-idllserveractivatableclassregistration">IDllServerActivatableClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration">RoGetActivatableClassRegistration</a>

