---
UID: NF:uiautomationcore.IUIAutomationRegistrar.RegisterProperty
title: IUIAutomationRegistrar::RegisterProperty (uiautomationcore.h)
description: Registers a third-party property.
helpviewer_keywords: ["IUIAutomationRegistrar interface [Windows Accessibility]","RegisterProperty method","IUIAutomationRegistrar.RegisterProperty","IUIAutomationRegistrar::RegisterProperty","RegisterProperty","RegisterProperty method [Windows Accessibility]","RegisterProperty method [Windows Accessibility]","IUIAutomationRegistrar interface","uiauto.uiauto_IUIAutomationRegistrar_RegisterProperty","uiauto_IUIAutomationRegistrar_RegisterProperty","uiautomationcore/IUIAutomationRegistrar::RegisterProperty","winauto.uiauto_IUIAutomationRegistrar_RegisterProperty"]
old-location: winauto\uiauto_IUIAutomationRegistrar_RegisterProperty.htm
tech.root: WinAuto
ms.assetid: 225bbbec-5910-4711-b713-3409c9925be2
ms.date: 12/05/2018
ms.keywords: IUIAutomationRegistrar interface [Windows Accessibility],RegisterProperty method, IUIAutomationRegistrar.RegisterProperty, IUIAutomationRegistrar::RegisterProperty, RegisterProperty, RegisterProperty method [Windows Accessibility], RegisterProperty method [Windows Accessibility],IUIAutomationRegistrar interface, uiauto.uiauto_IUIAutomationRegistrar_RegisterProperty, uiauto_IUIAutomationRegistrar_RegisterProperty, uiautomationcore/IUIAutomationRegistrar::RegisterProperty, winauto.uiauto_IUIAutomationRegistrar_RegisterProperty
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationRegistrar::RegisterProperty
 - uiautomationcore/IUIAutomationRegistrar::RegisterProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IUIAutomationRegistrar.RegisterProperty
---

# IUIAutomationRegistrar::RegisterProperty


## -description

Registers a third-party property.

## -parameters

### -param property [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiautomationpropertyinfo">UIAutomationPropertyInfo</a>*</b>

A pointer to a structure that contains information about the property to register.

### -param propertyId [out]

Type: <b>PropertyID*</b>

Receives the property ID of the newly registered property.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property ID can be used in various property methods, including <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue">GetCurrentPropertyValue</a>, and <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createpropertycondition">CreatePropertyCondition</a>. The same value can be used as a WinEvent value for property change events in <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a> implementations.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iuiautomationregistrar">IUIAutomationRegistrar</a>