---
UID: NF:d2d1.ID2D1Factory.GetDesktopDpi
title: ID2D1Factory::GetDesktopDpi
author: windows-sdk-content
description: Retrieves the current desktop dots per inch (DPI). To refresh this value, call ReloadSystemMetrics.
old-location: direct2d\ID2D1Factory_GetDesktopDpi.htm
tech.root: direct2d
ms.assetid: dd46252b-80eb-42c2-a2b4-5c49ef124bd5
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GetDesktopDpi, GetDesktopDpi method [Direct2D], GetDesktopDpi method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],GetDesktopDpi method, ID2D1Factory.GetDesktopDpi, ID2D1Factory::GetDesktopDpi, d2d1/ID2D1Factory::GetDesktopDpi, direct2d.ID2D1Factory_GetDesktopDpi
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory.GetDesktopDpi
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1.h
: 
- ID2D1Factory.GetDesktopDpi
: 
---

# ID2D1Factory::GetDesktopDpi


## -description


Retrieves the current desktop dots per inch (DPI). To refresh this value, call <a href="https://msdn.microsoft.com/32c831c4-73e1-49f8-8d58-4248ae99fe37">ReloadSystemMetrics</a>.


## -parameters




### -param dpiX [out]

Type: <b>FLOAT*</b>

 When this method returns, contains the horizontal DPI of the desktop. You must allocate storage for this parameter.


### -param dpiY [out]

Type: <b>FLOAT*</b>

When this method returns, contains the vertical DPI of the desktop. You must allocate storage for this parameter. 


## -returns



This method does not return a value.




## -remarks



Use this method to obtain the system DPI when setting physical pixel values, such as when you specify the size of a window.


#### Examples

The following code uses the <b>GetDesktopDpi</b> method to obtain the system DPI and set the initial size of a window.


```cpp

        // Because the CreateWindow function takes its size in pixels,
        // obtain the system DPI and use it to scale the window size.
        FLOAT dpiX, dpiY;

        // The factory returns the current system DPI. This is also the value it will use
        // to create its own windows.
        m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


        // Create the window.
        m_hwnd = CreateWindow(
            L"D2DDemoApp",
            L"Direct2D Demo App",
            WS_OVERLAPPEDWINDOW,
            CW_USEDEFAULT,
            CW_USEDEFAULT,
            static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
            static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
            NULL,
            NULL,
            HINST_THISCOMPONENT,
            this
            );

```


For more information about enabling high-DPI scenarios, see <a href="https://msdn.microsoft.com/72a4b076-1cf0-4dc9-bd75-43b5173fc2a0">How to Ensure that Your Application Displays Properly on High-DPI Displays</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/72a4b076-1cf0-4dc9-bd75-43b5173fc2a0">How to Ensure that Your Application Displays Properly on High-DPI Displays</a>



<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

