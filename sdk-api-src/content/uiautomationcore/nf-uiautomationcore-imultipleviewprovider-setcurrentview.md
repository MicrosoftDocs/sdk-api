---
UID: NF:uiautomationcore.IMultipleViewProvider.SetCurrentView
title: IMultipleViewProvider::SetCurrentView
author: windows-sdk-content
description: Sets the current control-specific view.
old-location: winauto\uiauto_IMultipleViewProvider_SetCurrentView.htm
tech.root: WinAuto
ms.assetid: dfa652be-b6b6-44e3-b06a-8ead56f17d2d
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMultipleViewProvider interface [Windows Accessibility],SetCurrentView method, IMultipleViewProvider.SetCurrentView, IMultipleViewProvider::SetCurrentView, SetCurrentView, SetCurrentView method [Windows Accessibility], SetCurrentView method [Windows Accessibility],IMultipleViewProvider interface, uiauto.uiauto_IMultipleViewProvider_SetCurrentView, uiauto_IMultipleViewProvider_SetCurrentView, uiautomationcore/IMultipleViewProvider::SetCurrentView, winauto.uiauto_IMultipleViewProvider_SetCurrentView
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
 - IMultipleViewProvider.SetCurrentView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMultipleViewProvider::SetCurrentView


## -description


Sets the current control-specific view. 


## -parameters




### -param viewId [in]

Type: <b>int</b>

A view identifier.
                


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



View identifiers can be retrieved by using <a href="https://msdn.microsoft.com/fd4d5616-c126-455e-84e7-e62e24daf8f9">IMultipleViewProvider::GetSupportedViews</a>.
        

The collection of view identifiers must be identical for all instances of a control.
            




## -see-also




<a href="https://msdn.microsoft.com/84d370a6-05bd-4efb-a6ca-99e9392f95dc">IMultipleViewProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

