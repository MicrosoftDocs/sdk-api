---
UID: NF:uiautomationcore.IUIAutomationPatternInstance.GetProperty
title: IUIAutomationPatternInstance::GetProperty
author: windows-sdk-content
description: The client wrapper object implements the IUIAutomation::get_CurrentX and IUIAutomationElement::get_CachedX methods by calling this function, specifying the property by index.
old-location: winauto\uiauto_IUIAutomationPatternInstance_GetProperty.htm
old-project: WinAuto
ms.assetid: cb64569f-799b-4e9a-a9f4-84513b98c941
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetProperty, GetProperty method [Windows Accessibility], GetProperty method [Windows Accessibility],IUIAutomationPatternInstance interface, IUIAutomationPatternInstance interface [Windows Accessibility],GetProperty method, IUIAutomationPatternInstance.GetProperty, IUIAutomationPatternInstance::GetProperty, uiauto.uiauto_IUIAutomationPatternInstance_GetProperty, uiauto_IUIAutomationPatternInstance_GetProperty, uiautomationcore/IUIAutomationPatternInstance::GetProperty, winauto.uiauto_IUIAutomationPatternInstance_GetProperty
ms.prod: windows
ms.technology: windows-sdk
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
 - IUIAutomationPatternInstance.GetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationPatternInstance::GetProperty


## -description


The client wrapper object implements the <b>IUIAutomation::get_Current</b><i>X</i> and <b>IUIAutomationElement::get_Cached</b><i>X</i> methods by calling this function, specifying the property by index. 


## -parameters




### -param index




### -param cached [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the property should be retrieved from the cache, otherwise <b>FALSE</b>.


### -param type [in]

Type: <b><a href="https://msdn.microsoft.com/6090d5b5-2376-43ce-bef2-49bb3515107a">UIAutomationType</a></b>

A value indicating the data type of the property.


### -param pPtr [out, retval]

Type: <b>void*</b>

Receives the value of the property.


#### - Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the property. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/54791426-3905-49d6-aaaf-87a18d3ef659">IUIAutomationPatternInstance</a>
 

 

