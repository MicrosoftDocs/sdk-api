---
UID: NS:uiautomationcore.UIAutomationParameter
title: UIAutomationParameter (uiautomationcore.h)
description: Contains information about a parameter of a custom control pattern.
helpviewer_keywords: ["UIAutomationParameter","UIAutomationParameter structure [Windows Accessibility]","uiauto.uiauto_UIAutomationParameterStruct","uiauto_UIAutomationParameterStruct","uiautomationcore/UIAutomationParameter","winauto.uiauto_UIAutomationParameterStruct"]
old-location: winauto\uiauto_UIAutomationParameterStruct.htm
tech.root: WinAuto
ms.assetid: 8287867d-5aaf-4c52-8a8b-d98de6a2ad4b
ms.date: 12/05/2018
ms.keywords: UIAutomationParameter, UIAutomationParameter structure [Windows Accessibility], uiauto.uiauto_UIAutomationParameterStruct, uiauto_UIAutomationParameterStruct, uiautomationcore/UIAutomationParameter, winauto.uiauto_UIAutomationParameterStruct
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
 - UIAutomationParameter
 - uiautomationcore/UIAutomationParameter
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
 - UIAutomationParameter
---

# UIAutomationParameter structure


## -description

Contains information about a parameter of a custom control pattern.

## -struct-fields

### -field type

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType</a></b>

A value indicating the type of the parameter.

### -field pData

Type: <b>void*</b>

A pointer to the parameter data.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod">CallMethod</a>



<a href="/windows/desktop/WinAuto/uiauto-custompropertieseventscontrolpatterns">Custom Properties, Events, and Control Patterns</a>



<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch">Dispatch</a>



<b>Reference</b>