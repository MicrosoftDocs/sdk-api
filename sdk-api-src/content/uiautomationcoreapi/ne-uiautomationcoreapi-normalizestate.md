---
UID: NE:uiautomationcoreapi.NormalizeState
title: NormalizeState (uiautomationcoreapi.h)
author: windows-sdk-content
description: Contains values that specify the behavior of UiaGetUpdatedCache.
old-location: winauto\uiauto_NormalizeStateEnum.htm
tech.root: WinAuto
ms.assetid: 242b3770-1082-4df9-b21b-cc78e587a2b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NormalizeState, NormalizeState enumeration [Windows Accessibility], NormalizeState_Custom, NormalizeState_None, NormalizeState_View, uiauto.uiauto_NormalizeStateEnum, uiauto_NormalizeStateEnum, uiautomationcoreapi/NormalizeState, uiautomationcoreapi/NormalizeState_Custom, uiautomationcoreapi/NormalizeState_None, uiautomationcoreapi/NormalizeState_View, winauto.uiauto_NormalizeStateEnum
ms.topic: enum
f1_keywords: ["uiautomationcoreapi/NormalizeState"]
req.header: uiautomationcoreapi.h
req.include-header: UIAutomation.h
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
 - NormalizeState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NormalizeState enumeration


## -description


Contains values that specify the behavior of <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiagetupdatedcache">UiaGetUpdatedCache</a>.


## -enum-fields




### -field NormalizeState_None

No normalization.


### -field NormalizeState_View

Normalize against the condition in the cache request specified by pRequest.


### -field NormalizeState_Custom

Normalize against the condition specified in pNormalizeCondition.

