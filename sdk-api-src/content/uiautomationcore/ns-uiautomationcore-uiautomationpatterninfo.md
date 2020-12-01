---
UID: NS:uiautomationcore.UIAutomationPatternInfo
title: UIAutomationPatternInfo (uiautomationcore.h)
description: Contains information about a custom control pattern.
helpviewer_keywords: ["UIAutomationPatternInfo","UIAutomationPatternInfo structure [Windows Accessibility]","uiauto.uiauto_UIAutomationPatternInfoStruct","uiauto_UIAutomationPatternInfoStruct","uiautomationcore/UIAutomationPatternInfo","winauto.uiauto_UIAutomationPatternInfoStruct"]
old-location: winauto\uiauto_UIAutomationPatternInfoStruct.htm
tech.root: WinAuto
ms.assetid: f45c5736-75f3-4e44-b92a-3b0a51b41849
ms.date: 12/05/2018
ms.keywords: UIAutomationPatternInfo, UIAutomationPatternInfo structure [Windows Accessibility], uiauto.uiauto_UIAutomationPatternInfoStruct, uiauto_UIAutomationPatternInfoStruct, uiautomationcore/UIAutomationPatternInfo, winauto.uiauto_UIAutomationPatternInfoStruct
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - UIAutomationPatternInfo
 - uiautomationcore/UIAutomationPatternInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCore.h
api_name:
 - UIAutomationPatternInfo
---

# UIAutomationPatternInfo structure


## -description

Contains information about a custom control pattern.

## -struct-fields

### -field guid

Type: <b>GUID</b>

The unique identifier of the control pattern.

### -field pProgrammaticName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the control pattern (a non-localizable string).

### -field providerInterfaceId

Type: <b>GUID</b>

The unique identifier of the provider interface for the control pattern.

### -field clientInterfaceId

Type: <b>GUID</b>

The unique identifier of the client interface for the control pattern.

### -field cProperties

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The count of elements in <b>pProperties</b>.

### -field pProperties

Type: <b><a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiautomationpropertyinfo">UIAutomationPropertyInfo</a>*</b>

A pointer to an array of structures describing properties available on the control pattern.

### -field cMethods

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The count of elements in <b>pMethods</b>.

### -field pMethods

Type: <b><a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiautomationmethodinfo">UIAutomationMethodInfo</a>*</b>

A pointer to an array of structures describing methods available on the control pattern.

### -field cEvents

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The count of elements in <b>pEvents</b>.

### -field pEvents

Type: <b><a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiautomationeventinfo">UIAutomationEventInfo</a>*</b>

A pointer to an array of structures describing events available on the control pattern.

### -field pPatternHandler

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iuiautomationpatternhandler">IUIAutomationPatternHandler</a>*</b>

A pointer to the object that makes the control pattern available to clients.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-custompropertieseventscontrolpatterns">Custom Properties, Events, and Control Patterns</a>



<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iuiautomationregistrar-registerpattern">RegisterPattern</a>