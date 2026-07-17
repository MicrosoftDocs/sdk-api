---
UID: NF:uiautomationcore.IUIAutomationClientInfo.get_ProcessName
tech.root: WinAuto
title: IUIAutomationClientInfo::get_ProcessName
ms.date: 01/14/2026
targetos: Windows
description: Gets the process name of the UI Automation client application.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: uiautomationcore.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows build 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - uiautomationcore.h
api_name:
 - IUIAutomationClientInfo::get_ProcessName
f1_keywords:
 - IUIAutomationClientInfo::get_ProcessName
 - uiautomationcore/IUIAutomationClientInfo::get_ProcessName
dev_langs:
 - c++
helpviewer_keywords:
 - get_ProcessName
---

# ProcessName function

## -description

Gets the process name of the UI Automation client application.

## -parameters

### -param processName [ out, retval]

The file name as a `BSTR`.

## -returns

S_OK - If process name retrieved successfully.

E_INVALIDARG - If *processName* parameter is null.

E_OUTOFMEMORY - If memory allocation for the process name failed.

## -remarks

Call [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free allocated memory.

## -see-also
