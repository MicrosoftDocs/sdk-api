---
UID: NS:uiautomationcoreapi.UiaCacheRequest
title: UiaCacheRequest (uiautomationcoreapi.h)
description: Note  This structure is deprecated.  Contains information about a request to cache data about UI Automation elements.
helpviewer_keywords: ["UiaCacheRequest","UiaCacheRequest structure [Windows Accessibility]","uiauto.uiauto_UiaCacheRequestStruct","uiauto_UiaCacheRequestStruct","uiautomationcoreapi/UiaCacheRequest","winauto.uiauto_UiaCacheRequestStruct"]
old-location: winauto\uiauto_UiaCacheRequestStruct.htm
tech.root: WinAuto
ms.assetid: 426355e4-50ce-4189-824d-c2256903224c
ms.date: 12/05/2018
ms.keywords: UiaCacheRequest, UiaCacheRequest structure [Windows Accessibility], uiauto.uiauto_UiaCacheRequestStruct, uiauto_UiaCacheRequestStruct, uiautomationcoreapi/UiaCacheRequest, winauto.uiauto_UiaCacheRequestStruct
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - UiaCacheRequest
 - uiautomationcoreapi/UiaCacheRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCoreApi.h
api_name:
 - UiaCacheRequest
---

# UiaCacheRequest structure


## -description

<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div>  Contains information about a request to cache data about UI Automation elements.

## -struct-fields

### -field pViewCondition

Type: <b>UiaCondition *</b>

The address of a <a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacondition">UiaCondition</a> structure that specifies the condition that cached elements must match.

### -field Scope

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a></b>

A value from the <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a> enumerated type indicating the scope of the cache request; for example, whether it includes children of the root element.

### -field pProperties

Type: <b>PROPERTYID*</b>

The address of an array of identifiers for properties to cache. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -field cProperties

Type: <b>int</b>

The count of elements in the <b>pProperties</b> array.

### -field pPatterns

Type: <b>PATTERNID*</b>

The address of an array of identifiers for control patterns to cache. For a list of control pattern IDs, see <a href="/windows/desktop/WinAuto/uiauto-controlpattern-ids">Control Pattern Identifiers</a>.

### -field cPatterns

Type: <b>int</b>

The count of elements in the <b>pPatterns</b> array.

### -field automationElementMode

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-automationelementmode">AutomationElementMode</a></b>

A value from the <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-automationelementmode">AutomationElementMode</a> enumerated type indicating the type of reference to cached UI Automation elements that is to be returned.