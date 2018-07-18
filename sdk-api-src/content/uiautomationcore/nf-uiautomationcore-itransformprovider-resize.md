---
UID: NF:uiautomationcore.ITransformProvider.Resize
title: ITransformProvider::Resize
author: windows-sdk-content
description: Resizes the control.
old-location: winauto\uiauto_ITransformProvider_Resize.htm
old-project: WinAuto
ms.assetid: ba22f770-1306-4c15-bc72-a928b91e0eb5
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: ITransformProvider interface [Windows Accessibility],Resize method, ITransformProvider.Resize, ITransformProvider::Resize, Resize, Resize method [Windows Accessibility], Resize method [Windows Accessibility],ITransformProvider interface, uiauto.uiauto_ITransformProvider_Resize, uiauto_ITransformProvider_Resize, uiautomationcore/ITransformProvider::Resize, winauto.uiauto_ITransformProvider_Resize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITransformProvider.Resize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITransformProvider::Resize


## -description


Resizes the control.


## -parameters




### -param width [in]

Type: <b>double</b>

The new width of the window in pixels.


### -param height [in]

Type: <b>double</b>

The new height of the window in pixels.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            When called on a control supporting split panes, this method might have the 
            side effect of resizing other contiguous panes. 
            


            An object cannot be moved, resized, or rotated such that its resulting screen location 
            would be completely outside the coordinates of its container and inaccessible to keyboard 
            or mouse. For example, a top-level window moved completely off-screen or a child object 
            moved outside the boundaries of the container's viewport. In these cases the object is 
            placed as close to the requested screen coordinates as possible with the top or left 
            coordinates overridden to be within the container boundaries.
            




## -see-also




<a href="https://msdn.microsoft.com/cdc2f81b-cf69-469f-9139-e9a73cf8c730">ITransformProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

