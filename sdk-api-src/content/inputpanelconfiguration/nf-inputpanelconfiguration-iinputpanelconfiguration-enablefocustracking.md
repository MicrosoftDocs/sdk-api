---
UID: NF:inputpanelconfiguration.IInputPanelConfiguration.EnableFocusTracking
title: IInputPanelConfiguration::EnableFocusTracking (inputpanelconfiguration.h)
description: Enables a client process to opt-in to the focus tracking mechanism for Windows Store apps that controls the invoking and dismissing semantics of the touch keyboard.
helpviewer_keywords: ["EnableFocusTracking","EnableFocusTracking method [Windows Shell]","EnableFocusTracking method [Windows Shell]","IInputPanelConfiguration interface","IInputPanelConfiguration interface [Windows Shell]","EnableFocusTracking method","IInputPanelConfiguration.EnableFocusTracking","IInputPanelConfiguration::EnableFocusTracking","inputpanelconfiguration/IInputPanelConfiguration::EnableFocusTracking","shell.iinputpanelconfiguration_enablefocustracking"]
old-location: shell\iinputpanelconfiguration_enablefocustracking.htm
tech.root: shell
ms.assetid: C20962EF-DB24-43EE-ADA6-4550163F9F73
ms.date: 12/05/2018
ms.keywords: EnableFocusTracking, EnableFocusTracking method [Windows Shell], EnableFocusTracking method [Windows Shell],IInputPanelConfiguration interface, IInputPanelConfiguration interface [Windows Shell],EnableFocusTracking method, IInputPanelConfiguration.EnableFocusTracking, IInputPanelConfiguration::EnableFocusTracking, inputpanelconfiguration/IInputPanelConfiguration::EnableFocusTracking, shell.iinputpanelconfiguration_enablefocustracking
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
 - IInputPanelConfiguration::EnableFocusTracking
 - inputpanelconfiguration/IInputPanelConfiguration::EnableFocusTracking
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
 - IInputPanelConfiguration.EnableFocusTracking
---

# IInputPanelConfiguration::EnableFocusTracking


## -description

Enables a client process to opt-in to the focus tracking mechanism for Windows Store apps  that controls the invoking and dismissing semantics of the touch keyboard.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  <p class="note">This method will not work in Windows 10. A user can manually configure settings through the notification center or through the <b>Typing</b> settings to enable pulling up a touch keyboard automatically when focusing on an edit control.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>
