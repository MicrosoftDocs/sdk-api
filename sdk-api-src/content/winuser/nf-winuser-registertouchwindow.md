---
UID: NF:winuser.RegisterTouchWindow
title: RegisterTouchWindow function (winuser.h)
description: Registers a window as being touch-capable.
helpviewer_keywords: ["RegisterTouchWindow","RegisterTouchWindow function [Windows Touch]","TWF_FINETOUCH","TWF_WANTPALM","wintouch.registertouchwindow","winuser/RegisterTouchWindow"]
old-location: wintouch\registertouchwindow.htm
tech.root: wintouch
ms.assetid: a70a7418-f79d-40c8-9219-3ce38a74da9f
ms.date: 12/05/2018
ms.keywords: RegisterTouchWindow, RegisterTouchWindow function [Windows Touch], TWF_FINETOUCH, TWF_WANTPALM, wintouch.registertouchwindow, winuser/RegisterTouchWindow
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
 - RegisterTouchWindow
 - winuser/RegisterTouchWindow
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
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - user32.dll
api_name:
 - RegisterTouchWindow
---

# RegisterTouchWindow function


## -description

Registers a window as being touch-capable.

## -parameters

### -param hwnd [in]

The handle of the window being registered. The function fails with <b>ERROR_ACCESS_DENIED</b> if the calling thread does not own the specified window.

### -param ulFlags [in]

A set of bit flags that specify optional modifications. This field may contain 0 or one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TWF_FINETOUCH"></a><a id="twf_finetouch"></a><dl>
<dt><b>TWF_FINETOUCH</b></dt>
</dl>
</td>
<td width="60%">
Specifies that <i>hWnd</i> prefers noncoalesced touch input.

</td>
</tr>
<tr>
<td width="40%"><a id="TWF_WANTPALM"></a><a id="twf_wantpalm"></a><dl>
<dt><b>TWF_WANTPALM</b></dt>
</dl>
</td>
<td width="60%">
Setting this flag disables palm rejection which reduces delays for getting <a href="/windows/desktop/wintouch/wm-touchdown">WM_TOUCH</a> messages. 
						     This is useful if you want as quick of a response as possible when a user touches your application.
						  

By default, palm detection is enabled and some <a href="/windows/desktop/wintouch/wm-touchdown">WM_TOUCH</a> messages are prevented from being sent 
						     to your application.  This is useful if you do not want to receive <b>WM_TOUCH</b> messages that are from palm contact.
                    

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

<div class="alert"><b>Note</b>  <b>RegisterTouchWindow</b> must be called on every window that will be used for touch input.  This means that if you have an application that has multiple windows within it, <b>RegisterTouchWindow</b> must be called on every window in that application that uses touch features. Also, an application can call <b>RegisterTouchWindow</b> any number of times for the same window if it desires to change the modifier flags. A window can be marked as no longer requiring touch input using the <a href="/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow">UnregisterTouchWindow</a> function.
  </div>
<div> </div>
If <b>TWF_WANTPALM</b> is enabled, packets from touch input are not buffered and palm detection is not performed before the packets are sent to your application. Enabling <b>TWF_WANTPALM</b> is most useful if you want minimal latencies when processing <a href="/windows/desktop/wintouch/wm-touchdown">WM_TOUCH</a> messages.


#### Examples


```cpp

BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in the global variable.

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   RegisterTouchWindow(hWnd, 0);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}	 
	 
```

## -see-also

<a href="/windows/desktop/wintouch/mtfunctions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow">UnregisterTouchWindow</a>