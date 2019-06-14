---
UID: NN:activation.IActivationFactory
title: IActivationFactory (activation.h)
author: windows-sdk-content
description: Enables classes to be activated by the Windows Runtime.
old-location: winrt\iactivationfactory.htm
tech.root: WinRT
ms.assetid: C6A2ED6E-9C45-4CF3-A301-72A5DAEB4DFC
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IActivationFactory, IActivationFactory interface [Windows Runtime], IActivationFactory interface [Windows Runtime],described, activation/IActivationFactory, winrt.iactivationfactory
ms.topic: interface
req.header: activation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Activation.idl
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
 - Activation.h
api_name:
 - IActivationFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActivationFactory interface


## -description


Enables classes to be activated by the Windows Runtime.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActivationFactory</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IActivationFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActivationFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/activation/nf-activation-iactivationfactory-activateinstance">ActivateInstance</a>
</td>
<td align="left" width="63%">
Creates a new instance of the Windows Runtime class that is associated with the current activation factory.

</td>
</tr>
</table> 


## -remarks



Implement the <b>IActivationFactory</b> interface when you create a class that you want Windows Runtime  applications to use. Clients call the <a href="https://docs.microsoft.com/windows/desktop/api/activation/nf-activation-iactivationfactory-activateinstance">ActivateInstance</a>method to use an instance of your class. 

You can get an <b>IActivationFactory</b> pointer by calling the <a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-rogetactivationfactory">RoGetActivationFactory</a> function.  

During activation of a class, the Windows Runtime calls the <a href="https://docs.microsoft.com/previous-versions//br205771(v=vs.85)">DllGetActivationFactory</a> function to get an <b>IActivationFactory</b> pointer that corresponds to the requested class. 




## -see-also




<a href="https://docs.microsoft.com/previous-versions//br205771(v=vs.85)">DllGetActivationFactory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-rogetactivationfactory">RoGetActivationFactory</a>
 

 

