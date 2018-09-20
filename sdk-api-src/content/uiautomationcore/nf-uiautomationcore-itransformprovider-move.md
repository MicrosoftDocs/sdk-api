---
UID: NF:uiautomationcore.ITransformProvider.Move
title: ITransformProvider::Move
author: windows-sdk-content
description: Moves the control.
old-location: winauto\uiauto_ITransformProvider_Move.htm
tech.root: WinAuto
ms.assetid: 5abd6b54-a555-4e6f-9868-9c9b3e2f6e50
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: ITransformProvider interface [Windows Accessibility],Move method, ITransformProvider.Move, ITransformProvider::Move, Move, Move method [Windows Accessibility], Move method [Windows Accessibility],ITransformProvider interface, uiauto.uiauto_ITransformProvider_Move, uiauto_ITransformProvider_Move, uiautomationcore/ITransformProvider::Move, winauto.uiauto_ITransformProvider_Move
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - UIAutomationCore.h
api_name:
 - ITransformProvider.Move
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransformProvider::Move


## -description


Moves the control. 


## -parameters




### -param x [in]

Type: <b>double</b>

The absolute screen coordinates of the left side of the control.


### -param y [in]

Type: <b>double</b>

The absolute screen coordinates of the top of the control.



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An object cannot be moved, resized or rotated such that its resulting screen 
        location would be completely outside the coordinates of its container and 
        inaccessible to keyboard or mouse. For example, when a top-level window is  
        moved completely off-screen or a child object is moved outside the boundaries 
        of the container's viewport. In these cases the object is placed as close to 
        the requested screen coordinates as possible with the top or left coordinates 
        overridden to be within the container boundaries.
		




## -see-also




<a href="https://msdn.microsoft.com/cdc2f81b-cf69-469f-9139-e9a73cf8c730">ITransformProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

