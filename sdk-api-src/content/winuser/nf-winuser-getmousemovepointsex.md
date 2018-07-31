---
UID: NF:winuser.GetMouseMovePointsEx
title: GetMouseMovePointsEx function
author: windows-sdk-content
description: Retrieves a history of up to 64 previous coordinates of the mouse or pen.
old-location: inputdev\getmousemovepointsex.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\getmousemovepointsex.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GMMP_USE_DISPLAY_POINTS, GMMP_USE_HIGH_RESOLUTION_POINTS, GetMouseMovePointsEx, GetMouseMovePointsEx function [Keyboard and Mouse Input], _win32_GetMouseMovePointsEx, _win32_getmousemovepointsex_cpp, inputdev.getmousemovepointsex, winui._win32_getmousemovepointsex, winuser/GetMouseMovePointsEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetMouseMovePointsEx
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetMouseMovePointsEx function


## -description


Retrieves a history of up to 64 previous coordinates of the mouse or pen.


## -parameters




### -param cbSize [in]

Type: <b>UINT</b>

The size, in bytes, of the <a href="https://msdn.microsoft.com/284d8fc1-6d24-4a8b-bd91-ba260c03df4f">MOUSEMOVEPOINT</a> structure. 


### -param lppt [in]

Type: <b>LPMOUSEMOVEPOINT</b>

A pointer to a <a href="https://msdn.microsoft.com/284d8fc1-6d24-4a8b-bd91-ba260c03df4f">MOUSEMOVEPOINT</a> structure containing valid mouse coordinates (in screen coordinates). It may also contain a time stamp. 

The <b>GetMouseMovePointsEx</b> function searches for the point in the mouse coordinates history. If the function finds the point, it returns the last 
						<i>nBufPoints</i> prior to and including the supplied point. 

If your application supplies a time stamp, the <b>GetMouseMovePointsEx</b> function will use it to differentiate between two equal points that were recorded at different times. 

An application should call this function using the mouse coordinates received from the <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a> message and convert them to screen coordinates. 


### -param lpptBuf [out]

Type: <b>LPMOUSEMOVEPOINT</b>

A pointer to a buffer that will receive the points. It should be at least 
					<i>cbSize</i>*
					<i>nBufPoints</i> in size. 


### -param nBufPoints [in]

Type: <b>int</b>

The number of points to be retrieved. 


### -param resolution [in]

Type: <b>DWORD</b>

The resolution desired. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GMMP_USE_DISPLAY_POINTS"></a><a id="gmmp_use_display_points"></a><dl>
<dt><b>GMMP_USE_DISPLAY_POINTS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Retrieves the points using the display resolution.

</td>
</tr>
<tr>
<td width="40%"><a id="GMMP_USE_HIGH_RESOLUTION_POINTS"></a><a id="gmmp_use_high_resolution_points"></a><dl>
<dt><b>GMMP_USE_HIGH_RESOLUTION_POINTS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Retrieves high resolution points. Points can range from zero to 65,535 (0xFFFF) in both x- and y-coordinates. This is the resolution provided by absolute coordinate pointing devices such as drawing tablets.

</td>
</tr>
</table>
 


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the number of points in the buffer. Otherwise, the function returns 
						–1. For extended error information, your application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The system retains the last 64 mouse coordinates and their time stamps. If your application supplies a mouse coordinate to <b>GetMouseMovePointsEx</b> and the coordinate exists in the system's mouse coordinate history, the function retrieves the specified number of coordinates from the systems' history. You can also supply a time stamp, which will be used to differentiate between identical points in the history.

The <b>GetMouseMovePointsEx</b> function will return points that eventually were dispatched not only to the calling thread but also to other threads.

<b>GetMouseMovePointsEx</b> may fail or return erroneous values in the following cases: 

<ul>
<li>If negative coordinates are passed in the <a href="https://msdn.microsoft.com/284d8fc1-6d24-4a8b-bd91-ba260c03df4f">MOUSEMOVEPOINT</a> structure. </li>
<li>If <b>GetMouseMovePointsEx</b> retrieves a coordinate with a negative value. </li>
</ul>
These situations can occur if multiple monitors are present. To correct this, first call 
				<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> to get the following values: 

<ul>
<li>SM_XVIRTUALSCREEN, </li>
<li>SM_YVIRTUALSCREEN, </li>
<li>SM_CXVIRTUALSCREEN, and </li>
<li>SM_CYVIRTUALSCREEN. </li>
</ul>
Then, for each point that is returned from <b>GetMouseMovePointsEx</b>, perform the following transform: 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>int nVirtualWidth = GetSystemMetrics(SM_CXVIRTUALSCREEN) ;
int nVirtualHeight = GetSystemMetrics(SM_CYVIRTUALSCREEN) ;
int nVirtualLeft = GetSystemMetrics(SM_XVIRTUALSCREEN) ;
int nVirtualTop = GetSystemMetrics(SM_YVIRTUALSCREEN) ;
int cpt = 0 ;
int mode = GMMP_USE_DISPLAY_POINTS ;

MOUSEMOVEPOINT mp_in ;
MOUSEMOVEPOINT mp_out[64] ;

ZeroMemory(&amp;mp_in, sizeof(mp_in)) ;
mp_in.x = pt.x &amp; 0x0000FFFF ;//Ensure that this number will pass through.
mp_in.y = pt.y &amp; 0x0000FFFF ;
cpt = GetMouseMovePointsEx(&amp;mp_in, &amp;mp_out, 64, mode) ;

for (int i = 0; i &lt; cpt; i++)
{
   switch(mode)
   {
   case GMMP_USE_DISPLAY_POINTS:
      if (mp_out[i].x &gt; 32767)
         mp_out[i].x -= 65536 ;
      if (mp_out[i].y &gt; 32767)
         mp_out[i].y -= 65536 ;
      break ;
   case GMMP_USE_HIGH_RESOLUTION_POINTS:
      mp_out[i].x = ((mp_out[i].x * (nVirtualWidth - 1)) - (nVirtualLeft * 65536)) / nVirtualWidth ;
      mp_out[i].y = ((mp_out[i].y * (nVirtualHeight - 1)) - (nVirtualTop * 65536)) / nVirtualHeight ;
      break ;
   }
} </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/284d8fc1-6d24-4a8b-bd91-ba260c03df4f">MOUSEMOVEPOINT</a>



<a href="https://msdn.microsoft.com/35f5e1ad-74d5-41bb-9016-b1c5de449550">Mouse Input</a>



<b>Reference</b>
 

 

