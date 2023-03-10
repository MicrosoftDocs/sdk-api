---
UID: NF:winuser.RealGetWindowClassA
tech.root: winmsg 
title: RealGetWindowClassA
ms.date: 04/14/2021
targetos: Windows
description: Retrieves a string that specifies the window type. (ANSI)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: User32.dll 
req.header: winuser.h
req.idl: 
req.include-header: Windows.h 
req.irql: 
req.kmdf-ver: 
req.lib: User32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only] 
req.target-min-winversvr: Windows 2000 Server [desktop apps only] 
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - RealGetWindowClassA
 - RealGetWindowClass
f1_keywords:
 - RealGetWindowClassA
 - winuser/RealGetWindowClassA
 - RealGetWindowClass
 - winuser/RealGetWindowClass
dev_langs:
 - c++
---

# RealGetWindowClassA function

## -description

Retrieves a string that specifies the window type.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window whose type will be retrieved.

### -param ptszClassName [out]

Type: <b>LPTSTR</b>

A pointer to a string that receives the window type.

### -param cchClassNameMax [in]

Type: <b>UINT</b>

The length, in characters, of the buffer pointed to by the <i>pszType</i> parameter.

## -returns

Type: <b>UINT</b>

If the function succeeds, the return value is the number of characters copied to the specified buffer. 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/winmsg/windows">Windows Overview</a>  
