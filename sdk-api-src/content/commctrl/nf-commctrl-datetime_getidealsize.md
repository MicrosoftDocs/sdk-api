---
UID: NF:commctrl.DateTime_GetIdealSize
title: DateTime_GetIdealSize macro (commctrl.h)
description: Gets the size needed to display the control without clipping. Use this macro or send the DTM_GETIDEALSIZE message explicitly.
helpviewer_keywords: ["DateTime_GetIdealSize","DateTime_GetIdealSize macro [Windows Controls]","_shell_DateTime_GetIdealSize","_shell_DateTime_GetIdealSize_cpp","commctrl/DateTime_GetIdealSize","controls.DateTime_GetIdealSize","controls._shell_DateTime_GetIdealSize"]
old-location: controls\DateTime_GetIdealSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getidealsize.htm
ms.date: 10/21/2024
ms.keywords: DateTime_GetIdealSize, DateTime_GetIdealSize macro [Windows Controls], _shell_DateTime_GetIdealSize, _shell_DateTime_GetIdealSize_cpp, commctrl/DateTime_GetIdealSize, controls.DateTime_GetIdealSize, controls._shell_DateTime_GetIdealSize
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DateTime_GetIdealSize
 - commctrl/DateTime_GetIdealSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - DateTime_GetIdealSize
---

# DateTime_GetIdealSize macro

## -syntax

```cpp
BOOL DateTime_GetIdealSize(
  [in]  HWND hdp,
  [out] SIZE psize
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b>.


## -description

Gets the size needed to display the control without clipping. Use this macro or send the <a href="/windows/desktop/Controls/dtm-getidealsize">DTM_GETIDEALSIZE</a> message explicitly.

## -parameters

### -param hdp [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the DTP control.

### -param psize [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-size">SIZE</a></b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure to receive the size. The caller is responsible for allocating this structure.
