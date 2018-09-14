---
UID: NF:uiautomationclient.IUIAutomationTransformPattern.Rotate
title: IUIAutomationTransformPattern::Rotate
author: windows-sdk-content
description: Rotates the UI Automation element.
old-location: winauto\uiauto_IUIAutomationTransformPattern_Rotate.htm
tech.root: WinAuto
ms.assetid: 97312397-dfea-435b-950d-6f346d5fa222
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IUIAutomationTransformPattern interface [Windows Accessibility],Rotate method, IUIAutomationTransformPattern.Rotate, IUIAutomationTransformPattern::Rotate, Rotate, Rotate method [Windows Accessibility], Rotate method [Windows Accessibility],IUIAutomationTransformPattern interface, uiauto.uiauto_IUIAutomationTransformPattern_Rotate, uiauto_IUIAutomationTransformPattern_Rotate, uiautomationclient/IUIAutomationTransformPattern::Rotate, winauto.uiauto_IUIAutomationTransformPattern_Rotate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - UIAutomationClient.h
api_name:
 - IUIAutomationTransformPattern.Rotate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTransformPattern::Rotate


## -description


Rotates the UI Automation element.


## -parameters




### -param degrees [in]

Type: <b>double</b>

The number of degrees to rotate the element. A positive number rotates clockwise; a negative number rotates counterclockwise.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An object cannot be moved, resized, or rotated such that its resulting screen location would be completely outside the coordinates of its container and inaccessible to the keyboard or mouse. For example, when a top-level window is moved completely off-screen or a child object is moved outside the boundaries of the container's viewport, the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.



