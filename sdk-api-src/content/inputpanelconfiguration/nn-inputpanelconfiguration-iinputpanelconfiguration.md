---
UID: NN:inputpanelconfiguration.IInputPanelConfiguration
title: IInputPanelConfiguration (inputpanelconfiguration.h)
description: Provides functionality for desktop apps to opt in to the focus tracking mechanism used in Windows Store apps.
old-location: shell\iinputpanelconfiguration.htm
tech.root: shell
ms.assetid: 81E54703-095E-4810-A8A0-2ACBE7F3D634
ms.date: 12/05/2018
ms.keywords: IInputPanelConfiguration, IInputPanelConfiguration interface [Windows Shell], IInputPanelConfiguration interface [Windows Shell],described, inputpanelconfiguration/IInputPanelConfiguration, shell.iinputpanelconfiguration
ms.topic: interface
f1_keywords:
- inputpanelconfiguration/IInputPanelConfiguration
dev_langs:
- c++
req.header: inputpanelconfiguration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inputpanelconfiguration.idl
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
- inputpanelconfiguration.h
api_name:
- IInputPanelConfiguration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInputPanelConfiguration interface


## -description


Provides functionality for desktop apps to opt in to the focus tracking mechanism used in Windows Store apps.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInputPanelConfiguration</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInputPanelConfiguration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInputPanelConfiguration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inputpanelconfiguration/nf-inputpanelconfiguration-iinputpanelconfiguration-enablefocustracking">EnableFocusTracking</a>
</td>
<td align="left" width="63%">
Enables a client process to opt-in to the focus tracking mechanism for Windows Store apps  that controls the invoking and dismissing semantics of the touch keyboard.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Warning</b>  <p class="note"><b>IInputPanelConfiguration</b> will not work in Windows 10. 

</div>
<div> </div>
Implement the <b>IInputPanelConfiguration</b> interface if your Desktop client processes need to leverage the invoking and dismissing semantics of the touch keyboard and handwriting input panel. 

The <b>IInputPanelConfiguration</b> interface enables your app to opt in to the focus tracking mechanism for Windows Store apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelinvocationconfiguration">IInputPanelInvocationConfiguration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

