---
UID: NF:wingdi.CreateHatchBrush
title: CreateHatchBrush function
author: windows-sdk-content
description: The CreateHatchBrush function creates a logical brush that has the specified hatch pattern and color.
old-location: gdi\createhatchbrush.htm
tech.root: gdi
ms.assetid: 0b5849d6-1e22-4ac5-980c-2f2a73b16adb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateHatchBrush, CreateHatchBrush function [Windows GDI], HS_BDIAGONAL, HS_CROSS, HS_DIAGCROSS, HS_FDIAGONAL, HS_HORIZONTAL, HS_VERTICAL, _win32_CreateHatchBrush, gdi.createhatchbrush, wingdi/CreateHatchBrush
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateHatchBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CreateHatchBrush
: 
---

# CreateHatchBrush function


## -description


The <b>CreateHatchBrush</b> function creates a logical brush that has the specified hatch pattern and color.


## -parameters




### -param iHatch [in]

The <a href="https://msdn.microsoft.com/ac0957db-242a-4d52-9661-2aa9d8571aab">hatch style of the brush</a>. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HS_BDIAGONAL"></a><a id="hs_bdiagonal"></a><dl>
<dt><b>HS_BDIAGONAL</b></dt>
</dl>
</td>
<td width="60%">
45-degree upward left-to-right hatch

</td>
</tr>
<tr>
<td width="40%"><a id="HS_CROSS"></a><a id="hs_cross"></a><dl>
<dt><b>HS_CROSS</b></dt>
</dl>
</td>
<td width="60%">
Horizontal and vertical crosshatch

</td>
</tr>
<tr>
<td width="40%"><a id="HS_DIAGCROSS"></a><a id="hs_diagcross"></a><dl>
<dt><b>HS_DIAGCROSS</b></dt>
</dl>
</td>
<td width="60%">
45-degree crosshatch

</td>
</tr>
<tr>
<td width="40%"><a id="HS_FDIAGONAL"></a><a id="hs_fdiagonal"></a><dl>
<dt><b>HS_FDIAGONAL</b></dt>
</dl>
</td>
<td width="60%">
45-degree downward left-to-right hatch

</td>
</tr>
<tr>
<td width="40%"><a id="HS_HORIZONTAL"></a><a id="hs_horizontal"></a><dl>
<dt><b>HS_HORIZONTAL</b></dt>
</dl>
</td>
<td width="60%">
Horizontal hatch

</td>
</tr>
<tr>
<td width="40%"><a id="HS_VERTICAL"></a><a id="hs_vertical"></a><dl>
<dt><b>HS_VERTICAL</b></dt>
</dl>
</td>
<td width="60%">
Vertical hatch

</td>
</tr>
</table>
 


### -param color [in]

The foreground color of the brush that is used for the hatches. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -returns



If the function succeeds, the return value identifies a logical brush.

If the function fails, the return value is <b>NULL</b>.




## -remarks



A brush is a bitmap that the system uses to paint the interiors of filled shapes.

After an application creates a brush by calling <b>CreateHatchBrush</b>, it can select that brush into any device context by calling the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function. It can also call <a href="https://msdn.microsoft.com/60e4467a-14ab-421e-b174-4b9c0134ce72">SetBkMode</a> to affect the rendering of the  brush.

If an application uses a hatch brush to fill the backgrounds of both a parent and a child window with matching color, you must  set the brush origin before painting the background of the child window. You can do this by  calling the <a href="https://msdn.microsoft.com/dcc7575a-49fd-4306-8baa-57e9e0d5ed1f">SetBrushOrgEx</a> function. Your application can retrieve the current brush origin by calling the <a href="https://msdn.microsoft.com/0b938237-cb06-4776-86f8-14478abcee00">GetBrushOrgEx</a> function.

When you no longer need the brush, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

<b>ICM:</b> No color is defined  at brush creation. However, color management is performed when the brush is selected into an ICM-enabled device context.


#### Examples

The following example creates a logical brush that has the specified hatch pattern and color. You can also  set a hatch brush background to transparent or to opaque.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#include &lt;windows.h&gt;
#include &lt;stdlib.h&gt;
#include &lt;string.h&gt;
#include &lt;tchar.h&gt;
#include &lt;stddef.h&gt;


#include &lt;gdiplus.h&gt;
#include &lt;assert.h&gt;

using namespace Gdiplus;

// Reference to the GDI+ static library).
#pragma comment (lib,"Gdiplus.lib")

// Global variables

// The main window class name.
static TCHAR szWindowClass[] = _T("win32app");


// The string that appears in the application's title bar.
static TCHAR szTitle[] = _T("Win32 Application Hatch Brush");

HINSTANCE hInst;

#define BTN_MYBUTTON_ID_1    503
#define BTN_MYBUTTON_ID_2    504


// Forward declarations of functions included in this code module:
LRESULT CALLBACK WndProc(HWND, UINT, WPARAM, LPARAM);

int WINAPI WinMain(HINSTANCE hInstance,
                   HINSTANCE hPrevInstance,
                   LPSTR lpCmdLine,
                   int nCmdShow)
{
    UNREFERENCED_PARAMETER(lpCmdLine);
    UNREFERENCED_PARAMETER(hPrevInstance);

    WNDCLASSEX wcex;

    wcex.cbSize = sizeof(WNDCLASSEX);
    wcex.style          = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc    = WndProc;
    wcex.cbClsExtra     = 0;
    wcex.cbWndExtra     = 0;
    wcex.hInstance      = hInstance;
    wcex.hIcon          = LoadIcon(hInstance, MAKEINTRESOURCE(IDI_APPLICATION));
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(COLOR_WINDOW+1);
    wcex.lpszMenuName   = NULL;
    wcex.lpszClassName  = szWindowClass;
    wcex.hIconSm        = LoadIcon(wcex.hInstance, MAKEINTRESOURCE(IDI_APPLICATION));

    if (!RegisterClassEx(&amp;wcex))
    {
        MessageBox(NULL,
            _T("Call to RegisterClassEx failed!"),
            _T("Win32 Guided Tour"),
            NULL);

        return 1;
    }

    hInst = hInstance; // Store instance handle in our global variable

    // The parameters to CreateWindow:
    // szWindowClass: the name of the application
    // szTitle: the text that appears in the title bar
    // WS_OVERLAPPEDWINDOW: the type of window to create
    // CW_USEDEFAULT, CW_USEDEFAULT: initial position (x, y)
    // 500, 100: initial size (width, length)
    // NULL: the parent of this window
    // NULL: this application does not have a menu bar
    // hInstance: the first parameter from WinMain
    // NULL: not used in this application
    HWND hWnd = CreateWindow(
        szWindowClass,
        szTitle,
        WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT, CW_USEDEFAULT,
        1000, 500,
        NULL,
        NULL,
        hInstance,
        NULL
    );

    if (!hWnd)
    {
        MessageBox(NULL,
            _T("Call to CreateWindow failed!"),
            _T("Win32 Guided Tour"),
            NULL);

        return 1;
    }

    // Create button controls.
    CreateWindowEx(NULL, L"BUTTON", L"Transparent", WS_VISIBLE | WS_CHILD,
        35, 35, 120, 20, hWnd, (HMENU)BTN_MYBUTTON_ID_1, NULL, NULL);

    CreateWindowEx(NULL, L"BUTTON", L"Opaque", WS_VISIBLE | WS_CHILD,
        35, 65, 120, 20, hWnd, (HMENU)BTN_MYBUTTON_ID_2, NULL, NULL);

    // The parameters to ShowWindow:
    // hWnd: the value returned from CreateWindow
    // nCmdShow: the fourth parameter from WinMain
    ShowWindow(hWnd,
        nCmdShow);
    UpdateWindow(hWnd);

    // Main message loop:
    MSG msg;
    while (GetMessage(&amp;msg, NULL, 0, 0))
    {
        TranslateMessage(&amp;msg);
        DispatchMessage(&amp;msg);
    }

    return (int) msg.wParam;
}

/***
 *    This function creates the following rectangles:
 *        1.    An outer rectangle using a solid brush with blue background.
 *        2.    An inner rectangle using a hatch brush with red horizontal lines and yellow background.
 *    It makes the background of the inner rectangle transparent or opaque in function of the user's input.
 *    Inputs: 
 *        1.    hdc, the display device context.
 *        2.    transparent, the hatch brush background user's value; true if transparent, false if opaque.
 ***/
VOID SetHatchBrushBackground(HDC hdc, bool transparent)
{
    // Define a brush handle.
    HBRUSH hBrush;

    // Create a solid blue brush.
    hBrush = CreateSolidBrush (RGB(0, 0, 255));

    // Associate the brush with the display device context.
    SelectObject (hdc, hBrush);

    // Draw a rectangle with blue background.
    Rectangle (hdc,  400,40,800,400);


    // Create a hatch brush that draws horizontal red lines.
    hBrush = CreateHatchBrush(HatchStyleHorizontal, RGB(255, 0, 0));

    // Set the background color to yellow.
    SetBkColor(hdc, RGB(255, 255, 0));


    // Select the hatch brush background transparency based on user's input.
    if (transparent == true)
        // Make the hatch brush background transparent.
        // This displays the outer rectangle blue background.
        SetBkMode(hdc, TRANSPARENT);
    else
        // Make the hatch brush background opaque.
        // This displays the inner rectangle yellow background.
        SetBkMode(hdc, OPAQUE);

    // Associate the hatch brush with the current device context.
    SelectObject(hdc, hBrush);

    // Draw a rectangle with the specified hatch brush.
    Rectangle(hdc,  500,130,700,300);

}

//
//  FUNCTION: WndProc(HWND, UINT, WPARAM, LPARAM)
//
//  PURPOSE:  Processes messages for the main window.
//
//  WM_PAINT    - Paint the main window
//  WM_DESTROY  - post a quit message and return
//
//
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    PAINTSTRUCT ps;
    HDC hdc;
    TCHAR greeting[] = _T("Select your brush background.");
    TCHAR wmId;
    TCHAR wmEvent;


    switch (message)
    {
    case WM_PAINT:
        hdc = BeginPaint(hWnd, &amp;ps);

        // Start application-specific layout section.
        // Just print the geeting string in the top left corner.
        TextOut(hdc,
            5, 5,
            greeting, (int)_tcslen(greeting));
        // End application-specific layout section.

        // Draw rectangles using hatch brush.
        SetHatchBrushBackground(hdc, true);


        EndPaint(hWnd, &amp;ps);
        break;

    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        hdc = GetDC(hWnd);

        switch (wmId) {

            case BTN_MYBUTTON_ID_1:
                // Draw the inner rectangle using a hatch brush transparent background.
                SetHatchBrushBackground(hdc, true);
                MessageBox(hWnd, _T("Hatch brush background is TRANSPARENT"), _T("Information"), MB_OK);
                break;

            case BTN_MYBUTTON_ID_2:
                // Draw the inner rectangle using a hatch brush opaque background.
                SetHatchBrushBackground(hdc, false);
                MessageBox(hWnd, _T("Hatch brush background is OPAQUE"), _T("Information"), MB_OK);
                break;
        }
        break;

    case WM_DESTROY:
        PostQuitMessage(0);
        break;


    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
        break;
    }

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/617eb778-876c-4bbb-90da-c5f13359becb">Brush Functions</a>



<a href="https://msdn.microsoft.com/b8912842-87d6-4d97-83ce-53d18cbedc74">Brushes Overview</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>



<a href="https://msdn.microsoft.com/0e34d108-fd35-4512-9eb3-c7710af36e95">CreateDIBPatternBrushPt</a>



<a href="https://msdn.microsoft.com/a3cf347e-9803-4bb0-bdb3-98929ef859ab">CreatePatternBrush</a>



<a href="https://msdn.microsoft.com/e39b5f77-97d8-4ea6-8277-7da12b3367f3">CreateSolidBrush</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/0b938237-cb06-4776-86f8-14478abcee00">GetBrushOrgEx</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>



<a href="https://msdn.microsoft.com/60e4467a-14ab-421e-b174-4b9c0134ce72">SetBkMode</a>



<a href="https://msdn.microsoft.com/dcc7575a-49fd-4306-8baa-57e9e0d5ed1f">SetBrushOrgEx</a>
 

 

