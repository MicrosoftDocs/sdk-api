---
UID: NF:uiautomationcore.IUIAutomationRegistrar.RegisterPattern
title: IUIAutomationRegistrar::RegisterPattern (uiautomationcore.h)
description: Registers a third-party control pattern.
helpviewer_keywords: ["IUIAutomationRegistrar interface [Windows Accessibility]","RegisterPattern method","IUIAutomationRegistrar.RegisterPattern","IUIAutomationRegistrar::RegisterPattern","RegisterPattern","RegisterPattern method [Windows Accessibility]","RegisterPattern method [Windows Accessibility]","IUIAutomationRegistrar interface","uiauto.uiauto_IUIAutomationRegistrar_RegisterPattern","uiauto_IUIAutomationRegistrar_RegisterPattern","uiautomationcore/IUIAutomationRegistrar::RegisterPattern","winauto.uiauto_IUIAutomationRegistrar_RegisterPattern"]
old-location: winauto\uiauto_IUIAutomationRegistrar_RegisterPattern.htm
tech.root: WinAuto
ms.assetid: 6aa61295-e035-4a51-9157-7cf9cfaee37a
ms.date: 12/05/2018
ms.keywords: IUIAutomationRegistrar interface [Windows Accessibility],RegisterPattern method, IUIAutomationRegistrar.RegisterPattern, IUIAutomationRegistrar::RegisterPattern, RegisterPattern, RegisterPattern method [Windows Accessibility], RegisterPattern method [Windows Accessibility],IUIAutomationRegistrar interface, uiauto.uiauto_IUIAutomationRegistrar_RegisterPattern, uiauto_IUIAutomationRegistrar_RegisterPattern, uiautomationcore/IUIAutomationRegistrar::RegisterPattern, winauto.uiauto_IUIAutomationRegistrar_RegisterPattern
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
 - IUIAutomationRegistrar::RegisterPattern
 - uiautomationcore/IUIAutomationRegistrar::RegisterPattern
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
 - IUIAutomationRegistrar.RegisterPattern
---

# IUIAutomationRegistrar::RegisterPattern


## -description

Registers a third-party control pattern.

## -parameters

### -param pattern [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiautomationpatterninfo">UIAutomationPatternInfo</a>*</b>

A pointer to a structure that contains information about the control pattern to register.

### -param pPatternId [out]

Type: <b>PATTERNID*</b>

Receives the pattern identifier.

### -param pPatternAvailablePropertyId [out]

Type: <b>PROPERTYID*</b>

Receives the property identifier for the pattern.  This value can be used with UI Automation client methods to determine whether the element supports the new pattern. This is equivalent to values such as <a href="/windows/desktop/WinAuto/uiauto-control-pattern-availability-propids">UIA_IsInvokePatternAvailablePropertyId</a>.

### -param propertyIdCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of properties supported by the control pattern.

### -param pPropertyIds [out]

Type: <b>PROPERTYID*</b>

Receives an array of identifiers for properties supported by the pattern.

### -param eventIdCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of events supported by the control pattern.

### -param pEventIds [out]

Type: <b>EVENTID*</b>

Receives an array of identifiers for events that are raised by the pattern.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The pattern, property, and event IDs retrieved by this method can be used in <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a> implementations.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iuiautomationregistrar">IUIAutomationRegistrar</a>