---
UID: NS:uiautomationclient.ExtendedProperty
title: ExtendedProperty (uiautomationclient.h)
description: Contains information about an extended property.
helpviewer_keywords: ["ExtendedProperty","ExtendedProperty structure [Windows Accessibility]","uiautomationclient/ExtendedProperty","winauto.uiauto_extendedproperty"]
old-location: winauto\uiauto_extendedproperty.htm
tech.root: WinAuto
ms.assetid: 3d0037f5-cff7-4502-b648-a2a60127eaff
ms.date: 12/05/2018
ms.keywords: ExtendedProperty, ExtendedProperty structure [Windows Accessibility], uiautomationclient/ExtendedProperty, winauto.uiauto_extendedproperty
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ExtendedProperty
 - uiautomationclient/ExtendedProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationClient.h
api_name:
 - ExtendedProperty
---

# ExtendedProperty structure


## -description

Contains information about an extended property.

## -struct-fields

### -field PropertyName

Type: <b>BSTR</b>

A localized string that contains the name of the extended property.

### -field PropertyValue

Type: <b>BSTR</b>

A string that represents the value of the extended property.   This string should be localized, if appropriate.

## -remarks

This structure is used by the <a href="/previous-versions/windows/desktop/legacy/hh437294(v=vs.85)">IUIAutomationStylesPattern::GetCachedExtendedPropertiesArray</a> and <a href="/previous-versions/windows/desktop/legacy/hh437295(v=vs.85)">GetCurrentExtendedPropertiesArray</a> methods.