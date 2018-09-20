---
UID: NF:uiautomationcore.IDockProvider.SetDockPosition
title: IDockProvider::SetDockPosition
author: windows-sdk-content
description: Sets the docking position of this element.
old-location: winauto\uiauto_IDockProvider_SetDockPosition.htm
tech.root: WinAuto
ms.assetid: 2e3d9a59-6bf4-4980-b318-f1badb0f8031
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IDockProvider interface [Windows Accessibility],SetDockPosition method, IDockProvider.SetDockPosition, IDockProvider::SetDockPosition, SetDockPosition, SetDockPosition method [Windows Accessibility], SetDockPosition method [Windows Accessibility],IDockProvider interface, uiauto.uiauto_IDockProvider_SetDockPosition, uiauto_IDockProvider_SetDockPosition, uiautomationcore/IDockProvider::SetDockPosition, winauto.uiauto_IDockProvider_SetDockPosition
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
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IDockProvider.SetDockPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDockProvider::SetDockPosition


## -description


Sets the docking position of this element. 


## -parameters






#### - dockPosition [in]

Type: <b><a href="https://msdn.microsoft.com/36ed98c2-f111-4192-8ce2-b8dd7da47de5">DockPosition</a></b>

The new docking position. 



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A docking container is a control that allows the arrangement of child elements, both horizontally and vertically, relative to the boundaries of the docking container and other elements within the container.




## -see-also




<a href="https://msdn.microsoft.com/106ca4b4-1304-4942-88a4-79a3895b552f">IDockProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

