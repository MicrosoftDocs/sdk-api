---
UID: NF:uiautomationcore.IMultipleViewProvider.GetSupportedViews
title: IMultipleViewProvider::GetSupportedViews
author: windows-sdk-content
description: Retrieves a collection of control-specific view identifiers.
old-location: winauto\uiauto_IMultipleViewProvider_GetSupportedViews.htm
old-project: WinAuto
ms.assetid: fd4d5616-c126-455e-84e7-e62e24daf8f9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSupportedViews, GetSupportedViews method [Windows Accessibility], GetSupportedViews method [Windows Accessibility],IMultipleViewProvider interface, IMultipleViewProvider interface [Windows Accessibility],GetSupportedViews method, IMultipleViewProvider.GetSupportedViews, IMultipleViewProvider::GetSupportedViews, uiauto.uiauto_IMultipleViewProvider_GetSupportedViews, uiauto_IMultipleViewProvider_GetSupportedViews, uiautomationcore/IMultipleViewProvider::GetSupportedViews, winauto.uiauto_IMultipleViewProvider_GetSupportedViews
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
 - Uiautomationcore.dll
api_name:
 - IMultipleViewProvider.GetSupportedViews
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMultipleViewProvider::GetSupportedViews


## -description


Retrieves a collection of control-specific view identifiers.


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a collection of control-specific integer values that identify the views available for a UI Automation element.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An empty array is returned by UIAutoCore.dll if the provider does not supply any view identifiers.
        

The collection of view identifiers must be identical for all instances of a control.
            

View identifier values can be passed to <a href="https://msdn.microsoft.com/72e9bca3-22cd-4f5b-9481-289bdfaf58e8">IMultipleViewProvider::GetViewName</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/84d370a6-05bd-4efb-a6ca-99e9392f95dc">IMultipleViewProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

