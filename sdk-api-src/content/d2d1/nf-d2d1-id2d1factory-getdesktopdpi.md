---
UID: NF:d2d1.ID2D1Factory.GetDesktopDpi
title: ID2D1Factory::GetDesktopDpi (d2d1.h)
description: Retrieves the current desktop dots per inch (DPI). To refresh this value, call ReloadSystemMetrics.
helpviewer_keywords: ["GetDesktopDpi","GetDesktopDpi method [Direct2D]","GetDesktopDpi method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","GetDesktopDpi method","ID2D1Factory.GetDesktopDpi","ID2D1Factory::GetDesktopDpi","d2d1/ID2D1Factory::GetDesktopDpi","direct2d.ID2D1Factory_GetDesktopDpi"]
old-location: direct2d\ID2D1Factory_GetDesktopDpi.htm
tech.root: Direct2D
ms.assetid: dd46252b-80eb-42c2-a2b4-5c49ef124bd5
ms.date: 12/05/2018
ms.keywords: GetDesktopDpi, GetDesktopDpi method [Direct2D], GetDesktopDpi method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],GetDesktopDpi method, ID2D1Factory.GetDesktopDpi, ID2D1Factory::GetDesktopDpi, d2d1/ID2D1Factory::GetDesktopDpi, direct2d.ID2D1Factory_GetDesktopDpi
f1_keywords:
- d2d1/ID2D1Factory.GetDesktopDpi
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Factory::GetDesktopDpi


## -description


Retrieves the current desktop dots per inch (DPI). To refresh this value, call <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-reloadsystemmetrics">ReloadSystemMetrics</a>.


## -parameters




### -param dpiX [out]

Type: <b>FLOAT*</b>

 When this method returns, contains the horizontal DPI of the desktop. You must allocate storage for this parameter.


### -param dpiY [out]

Type: <b>FLOAT*</b>

When this method returns, contains the vertical DPI of the desktop. You must allocate storage for this parameter. 


## -remarks



Use this method to obtain the system DPI when setting physical pixel values, such as when you specify the size of a window.


## Examples

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


For more information about enabling high-DPI scenarios, see <a href="/windows/win32/Direct2D/how-to--size-a-window-properly-for-high-dpi-displays">How to Ensure that Your Application Displays Properly on High-DPI Displays</a>.

<div class="code"></div>



## -see-also




<a href="/windows/win32/Direct2D/how-to--size-a-window-properly-for-high-dpi-displays">How to Ensure that Your Application Displays Properly on High-DPI Displays</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>
 

 

