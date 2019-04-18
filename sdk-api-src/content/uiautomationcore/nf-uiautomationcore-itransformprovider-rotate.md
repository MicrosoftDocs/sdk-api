---
UID: NF:uiautomationcore.ITransformProvider.Rotate
title: ITransformProvider::Rotate (uiautomationcore.h)
author: windows-sdk-content
description: Rotates the control.
old-location: winauto\uiauto_ITransformProvider_Rotate.htm
tech.root: WinAuto
ms.assetid: 2e8255de-b28d-4fc4-82ea-4255771f9838
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITransformProvider interface [Windows Accessibility],Rotate method, ITransformProvider.Rotate, ITransformProvider::Rotate, Rotate, Rotate method [Windows Accessibility], Rotate method [Windows Accessibility],ITransformProvider interface, uiauto.uiauto_ITransformProvider_Rotate, uiauto_ITransformProvider_Rotate, uiautomationcore/ITransformProvider::Rotate, winauto.uiauto_ITransformProvider_Rotate
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
 - ITransformProvider.Rotate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransformProvider::Rotate


## -description


Rotates the control.


## -parameters




### -param degrees [in]

Type: <b>double</b>

The number of degrees to rotate the control. 
				A positive number rotates clockwise; a negative number rotates counterclockwise.



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An object cannot be moved, resized, or rotated such that its resulting screen location 
            would be completely outside the coordinates of its container and inaccessible to keyboard 
            or mouse. For example, a top-level window moved completely off-screen or a child object 
            moved outside the boundaries of the container's viewport. In these cases the object is 
            placed as close to the requested screen coordinates as possible with the top or left 
            coordinates overridden to be within the container boundaries.
		




## -see-also




<a href="https://msdn.microsoft.com/cdc2f81b-cf69-469f-9139-e9a73cf8c730">ITransformProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

