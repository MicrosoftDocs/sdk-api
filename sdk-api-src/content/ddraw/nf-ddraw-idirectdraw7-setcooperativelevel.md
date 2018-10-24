---
UID: NF:ddraw.IDirectDraw7.SetCooperativeLevel
title: IDirectDraw7::SetCooperativeLevel
author: windows-sdk-content
description: Determines the top-level behavior of the application.
old-location: directdraw\idirectdraw7_setcooperativelevel.htm
tech.root: directdraw
ms.assetid: f791732d-9dab-470a-9243-6f71fd3bcd54
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DDSCL_ALLOWMODEX, DDSCL_ALLOWREBOOT, DDSCL_CREATEDEVICEWINDOW, DDSCL_EXCLUSIVE, DDSCL_FPUPRESERVE, DDSCL_FPUSETUP, DDSCL_FULLSCREEN, DDSCL_MULTITHREADED, DDSCL_NORMAL, DDSCL_NOWINDOWCHANGES, DDSCL_SETDEVICEWINDOW, DDSCL_SETFOCUSWINDOW, IDirectDraw7 interface [DirectDraw],SetCooperativeLevel method, IDirectDraw7.SetCooperativeLevel, IDirectDraw7::SetCooperativeLevel, SetCooperativeLevel, SetCooperativeLevel method [DirectDraw], SetCooperativeLevel method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::SetCooperativeLevel, directdraw.idirectdraw7_setcooperativelevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.SetCooperativeLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDraw7::SetCooperativeLevel


## -description


Determines the top-level behavior of the application.


## -parameters




### -param arg1

TBD


### -param arg2

TBD




#### - dwFlags [in]

This value consists of one or more of the following flags:



#### DDSCL_ALLOWMODEX

Allows the use of Mode X display modes. This flag can be used only if the DDSCL_EXCLUSIVE and DDSCL_FULLSCREEN flags are present.



#### DDSCL_ALLOWREBOOT

Allows CTRL+ALT+DEL to function while in exclusive (full-screen) mode.



#### DDSCL_CREATEDEVICEWINDOW

This flag is supported in Windows 98 and Windows 2000 only. Indicates that DirectDraw will create and manage a default device window for this DirectDraw object.



#### DDSCL_EXCLUSIVE

Requests the exclusive level. This flag must be used with the DDSCL_FULLSCREEN flag.



#### DDSCL_FPUPRESERVE

The calling application cares about the FPU state and does not want Direct3D to modify it in ways visible to the application. In this mode, Direct3D saves and restores the FPU state every time that it needs to modify the FPU state.



#### DDSCL_FPUSETUP

The calling application is likely to keep the FPU set up for optimal Direct3D performance (single precision and exceptions disabled), so Direct3D does not need to explicitly set the FPU each time. This is the default state.



#### DDSCL_FULLSCREEN

The exclusive-mode owner is responsible for the entire primary surface. The GDI can be ignored. This flag must be used with the DDSCL_EXCLUSIVE flag.



#### DDSCL_MULTITHREADED

Requests multithread-safe DirectDraw behavior. This causes Direct3D to take the global critical section more frequently.



#### DDSCL_NORMAL

The application functions as a typical Windows application. This flag cannot be used with the DDSCL_ALLOWMODEX, DDSCL_EXCLUSIVE, or DDSCL_FULLSCREEN flags.



#### DDSCL_NOWINDOWCHANGES

DirectDraw is not allowed to minimize or restore the application window on activation.



#### DDSCL_SETDEVICEWINDOW

This flag is supported in Windows 98 and Windows 2000 only. Indicates that the <i>hWnd</i> parameter is the window handle of the device window for this DirectDraw object. This flag cannot be used with the DDSCL_SETFOCUSWINDOW flag.



#### DDSCL_SETFOCUSWINDOW

This flag is supported in Windows 98 and Windows 2000 only. Indicates that the <i>hWnd</i> parameter is the window handle of the focus window for this DirectDraw object. This flag cannot be used with the DDSCL_SETDEVICEWINDOW flag.


#### - hWnd [in]

Window handle used for the application. Set to the calling application's top-level window handle (not a handle for any child windows created by the top-level window). This parameter can be NULL when the DDSCL_NORMAL flag is specified in the <i>dwFlags</i> parameter.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXCLUSIVEMODEALREADYSET</li>
<li>DDERR_HWNDALREADYSET</li>
<li>DDERR_HWNDSUBCLASSED</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>



## -remarks



This method must be called by the same thread that created the application window.



An application must set either the DDSCL_EXCLUSIVE or the DDSCL_NORMAL flag.



The DDSCL_EXCLUSIVE flag must be set to call functions that can adversely affect performance of other applications.

Interaction between this method and the <a href="https://msdn.microsoft.com/385918cd-64f1-449c-822a-0034a8184fb9">IDirectDraw7::SetDisplayMode</a> method differs from their IDirectDraw counterparts.

If you use Microsoft Foundation Classes (MFC), the window handle passed to this method must identify the application's top-level window, not a derived child window. To retrieve your MFC application's top-level window handle, you could use the following code:



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
HWND hwndTop = AfxGetMainWnd()-&gt;GetSafeHwnd();
</pre>
</td>
</tr>
</table></span></div>
You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>SetCooperativeLevel</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

