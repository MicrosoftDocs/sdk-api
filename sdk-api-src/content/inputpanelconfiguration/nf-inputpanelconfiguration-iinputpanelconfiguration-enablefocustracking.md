---
UID: NF:inputpanelconfiguration.IInputPanelConfiguration.EnableFocusTracking
title: IInputPanelConfiguration::EnableFocusTracking
author: windows-driver-content
description: Enables a client process to opt-in to the focus tracking mechanism for Windows Store apps that controls the invoking and dismissing semantics of the touch keyboard.
old-location: shell\iinputpanelconfiguration_enablefocustracking.htm
old-project: shell
ms.assetid: C20962EF-DB24-43EE-ADA6-4550163F9F73
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: EnableFocusTracking, EnableFocusTracking method [Windows Shell], EnableFocusTracking method [Windows Shell],IInputPanelConfiguration interface, IInputPanelConfiguration interface [Windows Shell],EnableFocusTracking method, IInputPanelConfiguration.EnableFocusTracking, IInputPanelConfiguration::EnableFocusTracking, inputpanelconfiguration/IInputPanelConfiguration::EnableFocusTracking, shell.iinputpanelconfiguration_enablefocustracking
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	inputpanelconfiguration.h
api_name:
-	IInputPanelConfiguration.EnableFocusTracking
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInputPanelConfiguration::EnableFocusTracking


## -description


Enables a client process to opt-in to the focus tracking mechanism for Windows Store apps  that controls the invoking and dismissing semantics of the touch keyboard.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  <p class="note">This method will not work in Windows 10. A user can manually configure settings through the notification center or through the <b>Typing</b> settings to enable pulling up a touch keyboard automatically when focusing on an edit control.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/81E54703-095E-4810-A8A0-2ACBE7F3D634">IInputPanelConfiguration</a>
 

 

