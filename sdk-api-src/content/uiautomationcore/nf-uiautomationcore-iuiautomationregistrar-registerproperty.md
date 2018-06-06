---
UID: NF:uiautomationcore.IUIAutomationRegistrar.RegisterProperty
title: IUIAutomationRegistrar::RegisterProperty
author: windows-sdk-content
description: Registers a third-party property.
old-location: winauto\uiauto_IUIAutomationRegistrar_RegisterProperty.htm
old-project: WinAuto
ms.assetid: 225bbbec-5910-4711-b713-3409c9925be2
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: IUIAutomationRegistrar interface [Windows Accessibility],RegisterProperty method, IUIAutomationRegistrar.RegisterProperty, IUIAutomationRegistrar::RegisterProperty, RegisterProperty, RegisterProperty method [Windows Accessibility], RegisterProperty method [Windows Accessibility],IUIAutomationRegistrar interface, uiauto.uiauto_IUIAutomationRegistrar_RegisterProperty, uiauto_IUIAutomationRegistrar_RegisterProperty, uiautomationcore/IUIAutomationRegistrar::RegisterProperty, winauto.uiauto_IUIAutomationRegistrar_RegisterProperty
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
req.idl: UIAutomationClient.idl
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
 - IUIAutomationRegistrar.RegisterProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationRegistrar::RegisterProperty


## -description


Registers a third-party property.


## -parameters




### -param property




### -param propertyId






#### - Property [in]

Type: <b><a href="https://msdn.microsoft.com/ea5b4cbe-5a39-407c-9c61-8e9ac4f3398f">UIAutomationPropertyInfo</a>*</b>

A pointer to a structure that contains information about the property to register.


#### - PropertyId [out]

Type: <b>PropertyID*</b>

Receives the property ID of the newly registered property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property ID can be used in various property methods, including <a href="https://msdn.microsoft.com/819e548e-7ff4-4f9f-969b-bfd1625f6151">GetCurrentPropertyValue</a>, and <a href="https://msdn.microsoft.com/8b777a53-90a8-4e51-b707-d0ea8f5790a8">CreatePropertyCondition</a>. The same value can be used as a WinEvent value for property change events in <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a> implementations.




## -see-also




<a href="https://msdn.microsoft.com/b5d979aa-7a87-4d6c-acdc-6e9eb19aac98">IUIAutomationRegistrar</a>
 

 

