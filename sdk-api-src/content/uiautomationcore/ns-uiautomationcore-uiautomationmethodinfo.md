---
UID: NS:uiautomationcore.UIAutomationMethodInfo
title: UIAutomationMethodInfo (uiautomationcore.h)
description: Contains information about a method that is supported by a custom control pattern.
helpviewer_keywords: ["UIAutomationMethodInfo","UIAutomationMethodInfo structure [Windows Accessibility]","uiauto.uiauto_UIAutomationMethodInfoStruct","uiauto_UIAutomationMethodInfoStruct","uiautomationcore/UIAutomationMethodInfo","winauto.uiauto_UIAutomationMethodInfoStruct"]
old-location: winauto\uiauto_UIAutomationMethodInfoStruct.htm
tech.root: WinAuto
ms.assetid: 33a52126-8757-44d0-91e1-758f51e3d0f8
ms.date: 12/05/2018
ms.keywords: UIAutomationMethodInfo, UIAutomationMethodInfo structure [Windows Accessibility], uiauto.uiauto_UIAutomationMethodInfoStruct, uiauto_UIAutomationMethodInfoStruct, uiautomationcore/UIAutomationMethodInfo, winauto.uiauto_UIAutomationMethodInfoStruct
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - UIAutomationMethodInfo
 - uiautomationcore/UIAutomationMethodInfo
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
 - UIAutomationMethodInfo
---

# UIAutomationMethodInfo structure


## -description

Contains information about a method that is supported by a custom control pattern.

## -struct-fields

### -field pProgrammaticName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The name of the method (a non-localizable string).

### -field doSetFocus

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if UI Automation should set the focus on the object before calling the method; otherwise <b>FALSE</b>.

### -field cInParameters

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The count of [in] parameters, which are always first in the <b>pParameterTypes</b> array.

### -field cOutParameters

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The count of [out] parameters, which always follow the [in] parameters in the <b>pParameterTypes</b> array.

### -field pParameterTypes

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType</a>*</b>

A pointer to an array of values indicating the data types of the parameters of the method. The data types of the In parameters should be first, followed by those of the Out parameters.

### -field pParameterNames

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a>*</b>

A pointer to an array containing the parameter names (non-localizable strings).

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-custompropertieseventscontrolpatterns">Custom Properties, Events, and Control Patterns</a>



<a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiautomationpatterninfo">UIAutomationPatternInfo</a>