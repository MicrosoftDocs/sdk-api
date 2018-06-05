---
UID: NF:uiautomationcore.IMultipleViewProvider.GetViewName
title: IMultipleViewProvider::GetViewName
author: windows-sdk-content
description: Retrieves the name of a control-specific view.
old-location: winauto\uiauto_IMultipleViewProvider_GetViewName.htm
old-project: WinAuto
ms.assetid: 72e9bca3-22cd-4f5b-9481-289bdfaf58e8
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: GetViewName, GetViewName method [Windows Accessibility], GetViewName method [Windows Accessibility],IMultipleViewProvider interface, IMultipleViewProvider interface [Windows Accessibility],GetViewName method, IMultipleViewProvider.GetViewName, IMultipleViewProvider::GetViewName, uiauto.uiauto_IMultipleViewProvider_GetViewName, uiauto_IMultipleViewProvider_GetViewName, uiautomationcore/IMultipleViewProvider::GetViewName, winauto.uiauto_IMultipleViewProvider_GetViewName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uiautomationcore.dll
api_name:
-	IMultipleViewProvider.GetViewName
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMultipleViewProvider::GetViewName


## -description


Retrieves the name of a control-specific view.


## -parameters




### -param viewId [in]

Type: <b>int</b>

A view identifier.


### -param pRetVal [out, retval]

Type: <b>BSTR*</b>

Receives a localized name for the view. 
                This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




            View identifiers can be retrieved by using <a href="https://msdn.microsoft.com/fd4d5616-c126-455e-84e7-e62e24daf8f9">IMultipleViewProvider::GetSupportedViews</a>.
            


            The collection of view identifiers must be identical for all instances of a control.
            


            View names must be suitable for use in text-to-speech, Braille, and other accessible applications.
            




## -see-also




<a href="https://msdn.microsoft.com/84d370a6-05bd-4efb-a6ca-99e9392f95dc">IMultipleViewProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

