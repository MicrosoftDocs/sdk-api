---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RegisterTouchWindow function


## -description


Registers a window as being touch-capable.


## -parameters




### -param hwnd

TBD


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

                       Setting this flag disables palm rejection which reduces delays for getting <a href="https://msdn.microsoft.com/5dee8bab-34fa-4dd9-a65b-35883757ec80">WM_TOUCH</a> messages. 
						     This is useful if you want as quick of a response as possible when a user touches your application.
						  

By default, palm detection is enabled and some <a href="https://msdn.microsoft.com/5dee8bab-34fa-4dd9-a65b-35883757ec80">WM_TOUCH</a> messages are prevented from being sent 
						     to your application.  This is useful if you do not want to receive <b>WM_TOUCH</b> messages that are from palm contact.
                    

</td>
</tr>
</table>
 


#### - hWnd [in]

The handle of the window being registered. The function fails with <b>ERROR_ACCESS_DENIED</b> if the calling thread does not own the specified window.


## -returns



If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> function.




## -remarks



<div class="alert"><b>Note</b>  <b>RegisterTouchWindow</b> must be called on every window that will be used for touch input.  This means that if you have an application that has multiple windows within it, <b>RegisterTouchWindow</b> must be called on every window in that application that uses touch features. Also, an application can call <b>RegisterTouchWindow</b> any number of times for the same window if it desires to change the modifier flags. A window can be marked as no longer requiring touch input using the <a href="https://msdn.microsoft.com/19b83312-b52b-45a5-9595-23d4621c4342">UnregisterTouchWindow</a> function.
  </div>
<div> </div>
If <b>TWF_WANTPALM</b> is enabled, packets from touch input are not buffered and palm detection is not performed before the packets are sent to your application. Enabling <b>TWF_WANTPALM</b> is most useful if you want minimal latencies when processing <a href="https://msdn.microsoft.com/5dee8bab-34fa-4dd9-a65b-35883757ec80">WM_TOUCH</a> messages.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
	 </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/19b83312-b52b-45a5-9595-23d4621c4342">UnregisterTouchWindow</a>
 

 

