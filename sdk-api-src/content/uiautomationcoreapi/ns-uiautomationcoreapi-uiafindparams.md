---
UID: NS:uiautomationcoreapi.UiaFindParams
title: UiaFindParams (uiautomationcoreapi.h)
description: Note  This structure is deprecated.  Contains parameters used in the UiaFind function.
helpviewer_keywords: ["UiaFindParams","UiaFindParams structure [Windows Accessibility]","uiauto.uiauto_UiaFindParamsStruct","uiauto_UiaFindParamsStruct","uiautomationcoreapi/UiaFindParams","winauto.uiauto_UiaFindParamsStruct"]
old-location: winauto\uiauto_UiaFindParamsStruct.htm
tech.root: WinAuto
ms.assetid: eb3c16d1-3e64-4f8e-aa03-c72c7a87b67f
ms.date: 12/05/2018
ms.keywords: UiaFindParams, UiaFindParams structure [Windows Accessibility], uiauto.uiauto_UiaFindParamsStruct, uiauto_UiaFindParamsStruct, uiautomationcoreapi/UiaFindParams, winauto.uiauto_UiaFindParamsStruct
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
 - UiaFindParams
 - uiautomationcoreapi/UiaFindParams
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
 - UiaFindParams
---

# UiaFindParams structure


## -description

<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div>  Contains parameters used in the <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiafind">UiaFind</a> function.

## -struct-fields

### -field MaxDepth

Type: <b>int</b>

The maximum depth to which to search the tree for matching elements.

### -field FindFirst

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to return only the first matching element; <b>FALSE</b> to return all matching elements.

### -field ExcludeRoot

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to exclude the root element; otherwise <b>FALSE</b>.

### -field pFindCondition

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacondition">UiaCondition</a>*</b>

Pointer to a <a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacondition">UiaCondition</a> structure that contains information about a condition that returned elements must match.