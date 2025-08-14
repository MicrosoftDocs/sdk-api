---
UID: NF:winuser.GetGestureConfig
title: GetGestureConfig function (winuser.h)
description: Retrieves the configuration for which Windows Touch gesture messages are sent from a window.
helpviewer_keywords: ["GetGestureConfig","GetGestureConfig function [Windows Touch]","wintouch.getgestureconfig","winuser/GetGestureConfig"]
old-location: wintouch\getgestureconfig.htm
tech.root: wintouch
ms.assetid: 8b7a594c-e9e4-4215-8946-da170c957a2b
ms.date: 12/05/2018
ms.keywords: GetGestureConfig, GetGestureConfig function [Windows Touch], wintouch.getgestureconfig, winuser/GetGestureConfig
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetGestureConfig
 - winuser/GetGestureConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - user32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetGestureConfig
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# GetGestureConfig function


## -description

Retrieves the configuration for which Windows  Touch gesture messages are sent from a window.

## -parameters

### -param hwnd [in]

A handle to the window to get the gesture configuration from.

### -param dwReserved [in]

This value is reserved and must be set to 0.

### -param dwFlags [in]

A gesture command flag value indicating options for retrieving the gesture configuration.  See Remarks for additional information and supported values.

### -param pcIDs [in]

The size, in number of gesture configuration structures, that is in the <i>pGestureConfig</i> buffer.

### -param pGestureConfig [in, out]

An array of gesture configuration structures that specify the gesture configuration.

### -param cbSize [in]

The size of the gesture configuration (<a href="/windows/desktop/api/winuser/ns-winuser-gestureconfig">GESTURECONFIG</a>) structure.

## -returns

If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

Passing a value other than <code>sizeof(GESTURECONFIG)</code> for the 
      <i>cbSize</i> parameter will cause calls to this function to fail and 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will 
      return <b>ERROR_INVALID_PARAMETER</b> (87 in decimal).    
      

The following table lists the gesture configuration values:
  

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>GCF_INCLUDE_ANCESTORS</b></td>
<td>0x00000001</td>
<td>If specified, <b>GetGestureConfig</b> returns consolidated configuration for the specified window and its parent window chain.</td>
</tr>
</table>
 


#### Examples


```cpp
    GESTURECONFIG gc[3];    
    UINT uiGcs = 3;

    ZeroMemory(&gc, sizeof(gc));
    gc[0].dwID  = GID_ZOOM;
    gc[1].dwID  = GID_ROTATE;
    gc[2].dwID  = GID_PAN;
    BOOL bResult = GetGestureConfig(hWnd, 0, 0, &uiGcs, gc, sizeof(GESTURECONFIG));        
    if (!bResult){                
        DWORD err = GetLastError();                                       
    }    

```

## -see-also

<a href="/windows/desktop/wintouch/mtgfunctions">Functions</a>



<a href="/windows/desktop/api/winuser/ns-winuser-gestureconfig">GESTURECONFIG</a>



<a href="/windows/desktop/wintouch/guide-multi-touch-gestures">Programming Guide for Gestures</a>
