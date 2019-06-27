---
UID: NF:uiautomationcore.IUIAutomationPatternInstance.GetProperty
title: IUIAutomationPatternInstance::GetProperty (uiautomationcore.h)
author: windows-sdk-content
description: The client wrapper object implements the IUIAutomation::get_CurrentX and IUIAutomationElement::get_CachedX methods by calling this function, specifying the property by index.
old-location: winauto\uiauto_IUIAutomationPatternInstance_GetProperty.htm
tech.root: WinAuto
ms.assetid: cb64569f-799b-4e9a-a9f4-84513b98c941
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [Windows Accessibility], GetProperty method [Windows Accessibility],IUIAutomationPatternInstance interface, IUIAutomationPatternInstance interface [Windows Accessibility],GetProperty method, IUIAutomationPatternInstance.GetProperty, IUIAutomationPatternInstance::GetProperty, uiauto.uiauto_IUIAutomationPatternInstance_GetProperty, uiauto_IUIAutomationPatternInstance_GetProperty, uiautomationcore/IUIAutomationPatternInstance::GetProperty, winauto.uiauto_IUIAutomationPatternInstance_GetProperty
ms.topic: method
f1_keywords: 
 - "uiautomationcore/IUIAutomationPatternInstance.GetProperty"
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
 - IUIAutomationPatternInstance.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationPatternInstance::GetProperty


## -description


The client wrapper object implements the <b>IUIAutomation::get_Current</b><i>X</i> and <b>IUIAutomationElement::get_Cached</b><i>X</i> methods by calling this function, specifying the property by index. 


## -parameters




### -param index [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the property. 


### -param cached [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the property should be retrieved from the cache, otherwise <b>FALSE</b>.


### -param arg3 [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType</a></b>

A value indicating the data type of the property.


### -param pPtr [out, retval]

Type: <b>void*</b>

Receives the value of the property.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iuiautomationpatterninstance">IUIAutomationPatternInstance</a>
 

 

