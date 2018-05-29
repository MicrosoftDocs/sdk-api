---
UID: NF:uiautomationcore.IUIAutomationPatternHandler.CreateClientWrapper
title: IUIAutomationPatternHandler::CreateClientWrapper
author: windows-sdk-content
description: Creates an object that enables a client application to interact with a custom control pattern.
old-location: winauto\uiauto_IUIAutomationPatternHandler_CreateClientWrapper.htm
old-project: WinAuto
ms.assetid: 03530381-52f8-4d9b-a54c-faebf7cd4a06
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: CreateClientWrapper, CreateClientWrapper method [Windows Accessibility], CreateClientWrapper method [Windows Accessibility],IUIAutomationPatternHandler interface, IUIAutomationPatternHandler interface [Windows Accessibility],CreateClientWrapper method, IUIAutomationPatternHandler.CreateClientWrapper, IUIAutomationPatternHandler::CreateClientWrapper, uiauto.uiauto_IUIAutomationPatternHandler_CreateClientWrapper, uiauto_IUIAutomationPatternHandler_CreateClientWrapper, uiautomationcore/IUIAutomationPatternHandler::CreateClientWrapper, winauto.uiauto_IUIAutomationPatternHandler_CreateClientWrapper
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.h
api_name:
-	IUIAutomationPatternHandler.CreateClientWrapper
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationPatternHandler::CreateClientWrapper


## -description


Creates an object that enables a client application to interact with a custom <i>control pattern</i>.


## -parameters




### -param pPatternInstance [in]

Type: <b><a href="https://msdn.microsoft.com/54791426-3905-49d6-aaaf-87a18d3ef659">IUIAutomationPatternInstance</a>*</b>

A pointer to the instance of the control pattern that will be used by the wrapper. 


### -param pClientWrapper [out, retval]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Receives a pointer to the wrapper object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The wrapper object exposes methods and properties of the <i>control pattern</i>. The implementation of the wrapper class passes these calls to Microsoft UI Automation by calling <a href="https://msdn.microsoft.com/a3c1aa20-c512-4752-8da6-c8e86bd56beb">CallMethod</a> and <a href="https://msdn.microsoft.com/cb64569f-799b-4e9a-a9f4-84513b98c941">GetProperty</a>. 
			




## -see-also




<a href="https://msdn.microsoft.com/6d0edd8e-3fd4-47d6-ab53-582eb81f38bd">IUIAutomationPatternHandler</a>
 

 

