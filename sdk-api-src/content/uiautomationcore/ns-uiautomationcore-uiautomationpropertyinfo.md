---
UID: NS:uiautomationcore.UIAutomationPropertyInfo
title: UIAutomationPropertyInfo (uiautomationcore.h)
description: Contains information about a custom property.
helpviewer_keywords: ["UIAutomationPropertyInfo","UIAutomationPropertyInfo structure [Windows Accessibility]","uiauto.uiauto_UIAutomationPropertyInfoStruct","uiauto_UIAutomationPropertyInfoStruct","uiautomationcore/UIAutomationPropertyInfo","winauto.uiauto_UIAutomationPropertyInfoStruct"]
old-location: winauto\uiauto_UIAutomationPropertyInfoStruct.htm
tech.root: WinAuto
ms.assetid: ea5b4cbe-5a39-407c-9c61-8e9ac4f3398f
ms.date: 12/05/2018
ms.keywords: UIAutomationPropertyInfo, UIAutomationPropertyInfo structure [Windows Accessibility], uiauto.uiauto_UIAutomationPropertyInfoStruct, uiauto_UIAutomationPropertyInfoStruct, uiautomationcore/UIAutomationPropertyInfo, winauto.uiauto_UIAutomationPropertyInfoStruct
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
 - UIAutomationPropertyInfo
 - uiautomationcore/UIAutomationPropertyInfo
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
 - UIAutomationPropertyInfo
---

# UIAutomationPropertyInfo structure


## -description

Contains information about a custom property.

## -struct-fields

### -field guid

Type: <b>GUID</b>

The unique identifier of the property.

### -field pProgrammaticName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The programmatic name of the property (a non-localizable string).

### -field type

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType</a> enumerated type indicating the data type of the property value.

## -remarks

A custom property must have one of the following data types specified by the <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType</a> enumeration. No other data types are supported for custom properties. For more information, see <a href="/windows/desktop/WinAuto/uiauto-custompropertieseventscontrolpatterns">Custom Properties, Events, and Control Patterns</a>.


<ul>
<li><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType_Bool</a></li>
<li><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType_Double</a></li>
<li><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType_Element</a></li>
<li><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType_Int</a></li>
<li><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType_Point</a></li>
<li><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-uiautomationtype">UIAutomationType_String</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-custompropertieseventscontrolpatterns">Custom Properties, Events, and Control Patterns</a>



<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iuiautomationregistrar-registerproperty">RegisterProperty</a>