---
UID: NF:uxtheme.BeginBufferedAnimation
title: BeginBufferedAnimation function
author: windows-sdk-content
description: Begins a buffered animation operation. The animation consists of a cross-fade between the contents of two buffers over a specified period of time.
old-location: controls\BeginBufferedAnimation.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\userex\functions\beginbufferedanimation.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BeginBufferedAnimation, BeginBufferedAnimation function [Windows Controls], _shell_BeginBufferedAnimation, _shell_BeginBufferedAnimation_cpp, controls.BeginBufferedAnimation, controls._shell_BeginBufferedAnimation, uxtheme/BeginBufferedAnimation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BP_BUFFERFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - BeginBufferedAnimation
product: Windows
targetos: Windows
req.lib: 
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# BeginBufferedAnimation function


## -description


Begins a buffered animation operation. The animation consists of a cross-fade between the contents of two buffers over a specified period of time.



## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window in which the animations play.


### -param hdcTarget

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

A handle of the target DC on which the buffer is animated.


### -param prcTarget

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a structure that specifies the area of the target DC in which to draw.


### -param dwFormat

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb759835(v=VS.85).aspx">BP_BUFFERFORMAT</a></b>

The format of the buffer.


### -param pPaintParams [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb773228(v=VS.85).aspx">BP_PAINTPARAMS</a>*</b>

A pointer to a structure that defines the paint operation parameters. This value can be <b>NULL</b>.


### -param pAnimationParams [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb773224(v=VS.85).aspx">BP_ANIMATIONPARAMS</a>*</b>

A pointer to a structure that defines the animation operation parameters.


### -param phdcFrom [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a>*</b>

When this function returns, this value points to the handle of the DC where the application should paint the initial state of the animation, if not <b>NULL</b>.


### -param phdcTo [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a>*</b>

When this function returns, this value points to the handle of the DC where the application should paint the final state of the animation, if not <b>NULL</b>.


## -returns



Type: <b>HANIMATIONBUFFER</b>

A handle to the buffered paint animation.




## -remarks



<b>BeginBufferedAnimation</b> will take care of drawing the intermediate frames between those two states by generating multiple <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> messages.
		

<b>BeginBufferedAnimation</b> starts a timer that generates <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> messages on which <a href="https://msdn.microsoft.com/en-us/library/Bb773271(v=VS.85).aspx">BufferedPaintRenderAnimation</a> should be called.  During these messages, <b>BufferedPaintRenderAnimation</b> will return <b>TRUE</b> when it paints an intermediate frame, to signify that the application has no further painting to do.

If the animation duration is zero, then only <i>phdcTo</i> is returned and <i>phdcFrom</i>  is set to <b>NULL</b>.  In this case, the application should paint the final state using <i>phdcTo</i> to get the behavior similar to <a href="https://msdn.microsoft.com/en-us/library/Bb773257(v=VS.85).aspx">BeginBufferedPaint</a>.




#### Examples

The following code example shows how to use this function. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;tchar.h&gt;
#include &lt;uxtheme.h&gt;

#pragma comment(lib, "uxtheme.lib")

#define WNDCLASSNAME L"BufferedPaintSample_WndClass"
#define ANIMATION_DURATION 500

bool g_fCurrentState = true;
bool g_fNewState = true;

void StartAnimation(HWND hWnd)
{
    g_fNewState = !g_fCurrentState;
    InvalidateRect(hWnd, NULL, TRUE);
}

void Paint(HWND hWnd, HDC hdc, bool state)
{
    RECT rc;
    GetClientRect(hWnd, &amp;rc);
    FillRect(hdc, &amp;rc, (HBRUSH)GetStockObject(WHITE_BRUSH));
    LPCTSTR pszIconId = state ? IDI_APPLICATION : IDI_ERROR;
    HICON hIcon = LoadIcon(NULL, pszIconId);
    if (hIcon)
    {
        DrawIcon(hdc, 10, 10, hIcon);
        DestroyIcon(hIcon);
    }
}

void OnPaint(HWND hWnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hWnd, &amp;ps);
    if (hdc)
    {
        // See if this paint was generated by a soft-fade animation
        if (!BufferedPaintRenderAnimation(hWnd, hdc))
        {
            BP_ANIMATIONPARAMS animParams;
            ZeroMemory(&amp;animParams, sizeof(animParams));
            animParams.cbSize = sizeof(BP_ANIMATIONPARAMS);
            animParams.style = BPAS_LINEAR;
            
            // Check if animation is needed. If not set dwDuration to 0
            animParams.dwDuration = (g_fCurrentState != g_fNewState ? ANIMATION_DURATION : 0);

            RECT rc;
            GetClientRect(hWnd, &amp;rc);

            HDC hdcFrom, hdcTo;
            HANIMATIONBUFFER hbpAnimation = BeginBufferedAnimation(hWnd, hdc, &amp;rc,
                BPBF_COMPATIBLEBITMAP, NULL, &amp;animParams, &amp;hdcFrom, &amp;hdcTo);
            if (hbpAnimation)
            {
                if (hdcFrom)
                {
                    Paint(hWnd, hdcFrom, g_fCurrentState);
                }
                if (hdcTo)
                {
                    Paint(hWnd, hdcTo, g_fNewState);
                }

                g_fCurrentState = g_fNewState;
                EndBufferedAnimation(hbpAnimation, TRUE);
            }
            else
            {
                Paint(hWnd, hdc, g_fCurrentState);
            }
        }
        
        EndPaint(hWnd, &amp;ps);
    }
}

LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_LBUTTONDOWN:
        StartAnimation(hWnd);
        break;
    case WM_PAINT:
        OnPaint(hWnd);
        break;
    case WM_SIZE:
        BufferedPaintStopAllAnimations(hWnd);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

int WINAPI _tWinMain(HINSTANCE hInstance,
     HINSTANCE hPrevInstance,
     LPSTR     lpCmdLine,
     int       nCmdShow)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    if (SUCCEEDED(BufferedPaintInit()))
    {
        WNDCLASSEX wcex;
        ZeroMemory(&amp;wcex, sizeof(wcex));
        wcex.cbSize = sizeof(WNDCLASSEX);
        wcex.style = CS_HREDRAW|CS_VREDRAW;
        wcex.lpfnWndProc = WndProc;
        wcex.hInstance = hInstance;
        wcex.hCursor = LoadCursor(NULL, IDC_ARROW);
        wcex.hIcon = LoadIcon(NULL, IDI_APPLICATION);
        wcex.lpszClassName = WNDCLASSNAME;
        RegisterClassEx(&amp;wcex);

        HWND hWnd = CreateWindow(WNDCLASSNAME, L"Buffered Paint Sample", 
            WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 0, 
            CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

        if (hWnd)
        {
            ShowWindow(hWnd, nCmdShow);
            UpdateWindow(hWnd);

            MSG msg;
            while (GetMessage(&amp;msg, NULL, 0, 0))
            {
                TranslateMessage(&amp;msg);
                DispatchMessage(&amp;msg);
            }
        }

        BufferedPaintUnInit();
    }

    return 0;
}
</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void BufferedPaint(HDC hdc, const RECT *prcPaint)
{
    BP_PAINTPARAMS paintParams = {0};
    paintParams.cbSize = sizeof(paintParams);

    HDC hdcBuffer;
    HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, prcPaint, 
        BPBF_COMPATIBLEBITMAP, &amp;paintParams, &amp;hdcBuffer);

    if (hBufferedPaint)
    {
        // Application specific painting code
        AppPaint(hdcBuffer, prcPaint);
        EndBufferedPaint(hBufferedPaint, TRUE);
    }
    else
    {
        // Error occurred, default to unbuffered painting
        AppPaint(hdc, prcPaint);
    }
}
</pre>
</td>
</tr>
</table></span></div>


