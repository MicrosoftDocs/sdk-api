---
UID: NN:inputpanelconfiguration.IInputPanelInvocationConfiguration
title: IInputPanelInvocationConfiguration (inputpanelconfiguration.h)
description: Enables Windows Store apps to opt out of the automatic invocation behavior.
helpviewer_keywords: ["IInputPanelInvocationConfiguration","IInputPanelInvocationConfiguration interface [Windows Shell]","IInputPanelInvocationConfiguration interface [Windows Shell]","described","inputpanelconfiguration/IInputPanelInvocationConfiguration","shell.iinputpanelinvocationconfiguration"]
old-location: shell\iinputpanelinvocationconfiguration.htm
tech.root: shell
ms.assetid: 452F46B6-3B71-4818-A528-B2A215EC9E87
ms.date: 12/05/2018
ms.keywords: IInputPanelInvocationConfiguration, IInputPanelInvocationConfiguration interface [Windows Shell], IInputPanelInvocationConfiguration interface [Windows Shell],described, inputpanelconfiguration/IInputPanelInvocationConfiguration, shell.iinputpanelinvocationconfiguration
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInputPanelInvocationConfiguration
 - inputpanelconfiguration/IInputPanelInvocationConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - inputpanelconfiguration.h
api_name:
 - IInputPanelInvocationConfiguration
---

# IInputPanelInvocationConfiguration interface


## -description

Enables Windows Store apps to opt out of the automatic invocation behavior.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInputPanelInvocationConfiguration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInputPanelInvocationConfiguration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInputPanelInvocationConfiguration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/inputpanelconfiguration/nf-inputpanelconfiguration-iinputpanelinvocationconfiguration-requiretouchineditcontrol">RequireTouchInEditControl</a>
</td>
<td align="left" width="63%">
Requires an explicit user tap in an edit field before the touch keyboard invokes.

</td>
</tr>
</table>

## -remarks

Clients can request that the touch keyboard and handwriting input panel check to see that a user tapped in the edit control with focus before invoking.

## -see-also

<a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>