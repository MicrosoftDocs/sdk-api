---
UID: NF:uiautomationcore.IUIAutomationPatternInstance.CallMethod
title: IUIAutomationPatternInstance::CallMethod
author: windows-sdk-content
description: Client wrapper implements methods by calling this CallMethod function, specifying the parameters as an array of pointers.
old-location: winauto\uiauto_IUIAutomationPatternInstance_CallMethod.htm
old-project: WinAuto
ms.assetid: a3c1aa20-c512-4752-8da6-c8e86bd56beb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CallMethod, CallMethod method [Windows Accessibility], CallMethod method [Windows Accessibility],IUIAutomationPatternInstance interface, IUIAutomationPatternInstance interface [Windows Accessibility],CallMethod method, IUIAutomationPatternInstance.CallMethod, IUIAutomationPatternInstance::CallMethod, uiauto.uiauto_IUIAutomationPatternInstance_CallMethod, uiauto_IUIAutomationPatternInstance_CallMethod, uiautomationcore/IUIAutomationPatternInstance::CallMethod, winauto.uiauto_IUIAutomationPatternInstance_CallMethod
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.redist: 
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
 - IUIAutomationPatternInstance.CallMethod
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationPatternInstance::CallMethod


## -description


Client wrapper implements methods by calling this CallMethod function, specifying the parameters as an array of pointers.


## -parameters




### -param index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the method. 


### -param pParams [in]

Type: <b><a href="https://msdn.microsoft.com/8287867d-5aaf-4c52-8a8b-d98de6a2ad4b">UIAutomationParameter</a>*</b>

 A pointer to an array of structures describing the parameters.


### -param cParams [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The count of parameters in <i>pParams</i>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/54791426-3905-49d6-aaaf-87a18d3ef659">IUIAutomationPatternInstance</a>
 

 

