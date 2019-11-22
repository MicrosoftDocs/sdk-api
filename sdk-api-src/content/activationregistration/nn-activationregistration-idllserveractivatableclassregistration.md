---
UID: NN:activationregistration.IDllServerActivatableClassRegistration
title: IDllServerActivatableClassRegistration (activationregistration.h)

description: Enables getting the registration info for an in-process server.
old-location: winrt\idllserveractivatableclassregistration.htm
tech.root: WinRT
ms.assetid: 00E9476E-45E0-4D97-9DA4-FD293674BED4

ms.date: 12/05/2018
ms.keywords: IDllServerActivatableClassRegistration, IDllServerActivatableClassRegistration interface [Windows Runtime], IDllServerActivatableClassRegistration interface [Windows Runtime],described, activationregistration/IDllServerActivatableClassRegistration, winrt.idllserveractivatableclassregistration
ms.topic: interface
f1_keywords: 
 - "activationregistration/IDllServerActivatableClassRegistration"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - activationregistration.h
api_name:
 - IDllServerActivatableClassRegistration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDllServerActivatableClassRegistration interface


## -description


Enables getting  the registration info for an in-process server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDllServerActivatableClassRegistration</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IDllServerActivatableClassRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDllServerActivatableClassRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-idllserveractivatableclassregistration-get_dllpath">get_DllPath</a>
</td>
<td align="left" width="63%">
Gets the fully qualified path to the in-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nf-activationregistration-idllserveractivatableclassregistration-get_threadingtype">get_ThreadingType</a>
</td>
<td align="left" width="63%">
Gets the apartment threading model for activating the in-process server.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nn-activationregistration-iactivatableclassregistration">IActivatableClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration">IExeServerActivatableClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>
 

 

