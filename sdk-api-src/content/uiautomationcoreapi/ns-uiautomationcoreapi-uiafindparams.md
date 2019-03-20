---
UID: NS:uiautomationcoreapi.UiaFindParams
title: UiaFindParams (uiautomationcoreapi.h)
author: windows-sdk-content
description: Note  This structure is deprecated.  Contains parameters used in the UiaFind function.
old-location: winauto\uiauto_UiaFindParamsStruct.htm
tech.root: WinAuto
ms.assetid: eb3c16d1-3e64-4f8e-aa03-c72c7a87b67f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UiaFindParams, UiaFindParams structure [Windows Accessibility], uiauto.uiauto_UiaFindParamsStruct, uiauto_UiaFindParamsStruct, uiautomationcoreapi/UiaFindParams, winauto.uiauto_UiaFindParamsStruct
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCoreApi.h
api_name:
 - UiaFindParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaFindParams structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div>  Contains parameters used in the <a href="https://msdn.microsoft.com/fe86b393-9c8d-46f1-85dc-5ac37f423ce0">UiaFind</a> function.


## -struct-fields




### -field MaxDepth

Type: <b>int</b>

The maximum depth to which to search the tree for matching elements.


### -field FindFirst

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to return only the first matching element; <b>FALSE</b> to return all matching elements.


### -field ExcludeRoot

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to exclude the root element; otherwise <b>FALSE</b>.


### -field pFindCondition

Type: <b><a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/82b5db01-08c9-4518-9d33-15d7813d0c80">UiaCondition</a> structure that contains information about a condition that returned elements must match.

