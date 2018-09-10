---
UID: NF:uiautomationclient.IUIAutomationTransformPattern.Move
title: IUIAutomationTransformPattern::Move
author: windows-sdk-content
description: Moves the UI Automation element.
old-location: winauto\uiauto_IUIAutomationTransformPattern_Move.htm
tech.root: WinAuto
ms.assetid: 6529de7b-cb7d-4e18-b274-bc6bf003f912
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IUIAutomationTransformPattern interface [Windows Accessibility],Move method, IUIAutomationTransformPattern.Move, IUIAutomationTransformPattern::Move, Move, Move method [Windows Accessibility], Move method [Windows Accessibility],IUIAutomationTransformPattern interface, uiauto.uiauto_IUIAutomationTransformPattern_Move, uiauto_IUIAutomationTransformPattern_Move, uiautomationclient/IUIAutomationTransformPattern::Move, winauto.uiauto_IUIAutomationTransformPattern_Move
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
 - IUIAutomationTransformPattern.Move
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTransformPattern::Move


## -description


Moves the UI Automation element.


## -parameters




### -param x [in]

Type: <b>double</b>

Absolute screen coordinates of the left side of the control.


### -param y [in]

Type: <b>double</b>

Absolute screen coordinates of the top of the control.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An element cannot be moved, resized or rotated such that its resulting screen location would be completely outside the coordinates of its container and inaccessible to the keyboard or mouse. For example, when a top-level window is moved completely off-screen or a child object is moved outside the boundaries of the container's viewport, the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.




## -see-also




<a href="https://msdn.microsoft.com/b2c91a4c-8f22-4ad8-8ce7-ed6469af4426">CachedCanMove</a>



<a href="https://msdn.microsoft.com/c8b198a7-2b07-4dab-9cb5-95cf8f73cb57">CurrentCanMove</a>



<a href="https://msdn.microsoft.com/276b44d9-a335-4d4e-8fe9-de03584dadb4">IUIAutomationTransformPattern</a>
 

 

