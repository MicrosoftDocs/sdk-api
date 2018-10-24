---
UID: NF:uiautomationcore.IVirtualizedItemProvider.Realize
title: IVirtualizedItemProvider::Realize
author: windows-sdk-content
description: Makes the virtual item fully accessible as a UI Automation element.
old-location: winauto\uiauto_IVirtualizedItemProvider_Realize.htm
tech.root: WinAuto
ms.assetid: ec69f0d2-a643-4f1b-892a-0d90f79afe72
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: IVirtualizedItemProvider interface [Windows Accessibility],Realize method, IVirtualizedItemProvider.Realize, IVirtualizedItemProvider::Realize, Realize, Realize method [Windows Accessibility], Realize method [Windows Accessibility],IVirtualizedItemProvider interface, uiauto.uiauto_IVirtualizedItemProvider_Realize, uiauto_IVirtualizedItemProvider_Realize, uiautomationcore/IVirtualizedItemProvider::Realize, winauto.uiauto_IVirtualizedItemProvider_Realize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IVirtualizedItemProvider.Realize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVirtualizedItemProvider::Realize


## -description


Makes the virtual item fully accessible as a UI Automation element.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When an item is obtained from a virtual list, it is only a placeholder. Use this method to convert it to a full reference to UI Automation element. 
	




## -see-also




<a href="https://msdn.microsoft.com/39baaa54-b836-497c-b401-a865202626e7">IVirtualizedItemProvider</a>
 

 

