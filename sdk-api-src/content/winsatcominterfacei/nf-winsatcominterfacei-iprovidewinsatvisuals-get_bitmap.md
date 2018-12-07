---
UID: NF:winsatcominterfacei.IProvideWinSATVisuals.get_Bitmap
title: IProvideWinSATVisuals::get_Bitmap
author: windows-sdk-content
description: Retrieves a bitmap for the WinSAT base score.
old-location: winsat\iprovidewinsatvisuals_get_bitmap.htm
tech.root: WinSAT
ms.assetid: 90188fb1-3125-459e-a475-5042c2ee0a5c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IProvideWinSATVisuals interface [WinSAT],get_Bitmap method, IProvideWinSATVisuals.get_Bitmap, IProvideWinSATVisuals::get_Bitmap, get_Bitmap, get_Bitmap method [WinSAT], get_Bitmap method [WinSAT],IProvideWinSATVisuals interface, winsat.iprovidewinsatvisuals_get_bitmap, winsatcominterfacei/IProvideWinSATVisuals::get_Bitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsatcominterfacei.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Winsatapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IProvideWinSATVisuals.get_Bitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProvideWinSATVisuals::get_Bitmap


## -description


<p class="CCE_Message">[IProvideWinSATVisuals::get_Bitmap may be altered or unavailable for releases after Windows 8.1.]

Retrieves a bitmap for the WinSAT base score.


## -parameters




### -param bitmapSize [in]

Determines the size of the bitmap that this method returns. For possible values, see the <a href="https://msdn.microsoft.com/5cc91824-f3d4-4c33-85df-b98c8d6ac0a1">WINSAT_BITMAP_SIZE</a> enumeration.


### -param state [in]

The state of the assessment. To get this value, call the <a href="https://msdn.microsoft.com/57a373f9-47b0-48cc-8517-cba87367c64e">IProvideWinSATResultsInfo::get_AssessmentState</a> method.


### -param rating [in]

The base score for the computer. To get this value, call the <a href="https://msdn.microsoft.com/4fe20830-bf86-4551-ba73-534740cabab5">IProvideWinSATResultsInfo::get_SystemRating</a> method.


### -param pBitmap [out]

The handle to the bitmap. To free the handle when finished, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function.


## -returns



This method can return one of these values.


The following table lists some of the HRESULT values that this method returns.





<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved the bitmap.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINSAT_ERROR_FAILEDTOLOADRESOURCE</b></dt>
<dt>0x80040016</dt>
</dl>
</td>
<td width="60%">
The <i>rating</i> value is not valid. Valid values are 1.0 through 9.9.

</td>
</tr>
</table>
 




## -remarks



The bitmap is returned only for the WINSAT_ASSESSMENT_STATE_VALID and WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE states. The method will succeed (return value is S_OK) if you pass another state value, but the <i>pBitmap</i> parameter will be <b>NULL</b>.


#### Examples

The following example shows how to retrieve a bitmap that represents the base score of the assessment. The example uses the <a href="https://msdn.microsoft.com/adf4de42-9dfd-46a7-ae75-3bbcfd15dd68">Win32_WinSAT</a> WMI MOF class to get the state and base score that you pass to this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;comutil.h&gt;
#include &lt;commctrl.h&gt;
#include &lt;wbemidl.h&gt;
#include &lt;winsatcominterfacei.h&gt;

#pragma comment(lib, "comsupp.lib") // For _bstr_t
#pragma comment(lib, "comctl32.lib") // For common controls
#pragma comment(lib, "gdi32.lib")

// The WQL query used to retrieve an instance of the Win32_WinSAT class.
#define WINSAT_QUERY_STRING  L"Select * \
From Win32_WinSAT \
Where TimeTaken = 'MostRecentAssessment'"

HRESULT GetBaseScore(float* pBaseScore, WINSAT_ASSESSMENT_STATE* pState);
HRESULT GetScoreBitmap(const float BaseScore, const WINSAT_ASSESSMENT_STATE State, HBITMAP* phbitmap);
LRESULT CALLBACK MonitorWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam);

// Global variables
HINSTANCE g_hinst;
HWND g_hwndStatus;
HBITMAP g_hScoreBitmap;

#define IDC_MONITOR        100

int WINAPI WinMain(HINSTANCE hinst,
    HINSTANCE hinstPrev,
    LPSTR pszCmdLine,
    int nCmdShow)
{
    WNDCLASSEX wc;
    ATOM atom;
    HWND hwnd;
    MSG msg;

    g_hinst = hinst;

    ZeroMemory(&amp;wc, sizeof(wc));
    wc.cbSize = sizeof(wc);
    wc.lpfnWndProc = MonitorWndProc;
    wc.hInstance = hinst;
    wc.lpszClassName = TEXT("MainWClass");
    wc.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);
    wc.hCursor = LoadCursor(NULL, IDC_ARROW);

    atom = RegisterClassEx(&amp;wc);
    hwnd = CreateWindowEx(0,
        TEXT("MainWClass"),
        TEXT("Experience Index Base Score"),
        WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN,
        CW_USEDEFAULT, CW_USEDEFAULT, 
        390, 165, 
        NULL,
        NULL,
        hinst,
        NULL);

    if (NULL == hwnd)
    {
        return (int)GetLastError();
    }

    ShowWindow(hwnd, nCmdShow);

    while (GetMessage(&amp;msg, NULL, 0, 0))
    {
        TranslateMessage(&amp;msg);
        DispatchMessage(&amp;msg);
    }

    return (int)msg.wParam;
}


LRESULT CALLBACK MonitorWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam)
{
    HRESULT  hr = S_OK;

    switch(msg)
    {
        case WM_CREATE:
        {
            INITCOMMONCONTROLSEX initctrls;
            RECT rc;
            float BaseScore = 0.0;
            WINSAT_ASSESSMENT_STATE AssessmentState;

            SetWindowText(hwnd, TEXT("Experience Index Base Score"));

            initctrls.dwSize = sizeof(initctrls);
            initctrls.dwICC = ICC_BAR_CLASSES;
            InitCommonControlsEx(&amp;initctrls);

            GetClientRect(hwnd, &amp;rc);

            g_hwndStatus = CreateWindowEx(0, STATUSCLASSNAME, NULL,
                WS_CHILD | WS_BORDER | WS_VISIBLE,
                rc.left, rc.bottom - 20, rc.right, 20,
                hwnd, (HMENU) IDC_MONITOR, g_hinst, NULL);
                
            if (NULL == g_hwndStatus)
                return (LRESULT) NULL;

            hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

            // Get the base score and the state of the assessment.
            if (FAILED(hr = GetBaseScore(&amp;BaseScore, &amp;AssessmentState)))
            {
                SetWindowText(g_hwndStatus, TEXT("Failed to get base score and state"));
            }

            // Get the bitmap for the specified score and state values.
            if (FAILED(hr = GetScoreBitmap(BaseScore, AssessmentState, &amp;g_hScoreBitmap)) || NULL == g_hScoreBitmap)
            {
                SetWindowText(g_hwndStatus, TEXT("Failed to get base score bitmap"));
            }

            break;
        }

        case WM_PAINT:
            PAINTSTRUCT ps;
            HDC hdcWin;
            HDC hdcCompatible;
            HGDIOBJ bmpOld;
            BITMAP bitmap;

            // Write the bitmap to the window.
            if (g_hScoreBitmap)
            {
                hdcWin = BeginPaint(hwnd, &amp;ps);
                hdcCompatible = CreateCompatibleDC(hdcWin);
                bmpOld = SelectObject(hdcCompatible, g_hScoreBitmap);
                GetObject(g_hScoreBitmap, sizeof(BITMAP), &amp;bitmap);
                BitBlt(hdcWin, 0, 0, bitmap.bmWidth, bitmap.bmHeight, hdcCompatible, 0, 0, SRCCOPY);
                SelectObject(hdcCompatible, bmpOld);
                DeleteDC(hdcCompatible);
                EndPaint(hwnd, &amp;ps);
            }

            break;

        case WM_CLOSE:
            DestroyWindow(hwnd);
            break;

        case WM_DESTROY:
            CoUninitialize();
            DeleteObject(g_hScoreBitmap);
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wparam, lparam);
    }

    return 0;
}

// Use the Win32_WinSAT WMI class to retrieve the base score and
// state of the most recent assessmeent.
HRESULT GetBaseScore(float* pBaseScore, WINSAT_ASSESSMENT_STATE* pState)
{
    HRESULT hr = S_OK;
    IWbemServices* pServices = NULL;
    IWbemLocator* pLocator = NULL;
    IEnumWbemClassObject* pEnum = NULL;
    IWbemClassObject* pWinSAT = NULL;
    _variant_t vBaseScore;
    _variant_t vState;
    ULONG returned = 0;

    // WMI code to retrieve the Win32_WinSAT instance.
    hr = CoCreateInstance(__uuidof(WbemLocator),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IWbemLocator),
        (void**)&amp;pLocator);

    if (FAILED(hr))
    {
        // Handle error
        goto cleanup;
    }

    hr = pLocator-&gt;ConnectServer(_bstr_t(L"root\\cimv2"), 
        NULL, NULL, NULL, 0L, NULL, NULL,
        &amp;pServices);

    if (FAILED(hr))
    {
        // Handle error
        goto cleanup;
    }
    
    hr = pServices-&gt;ExecQuery(_bstr_t(L"WQL"),
        _bstr_t(WINSAT_QUERY_STRING),
        WBEM_FLAG_USE_AMENDED_QUALIFIERS | WBEM_FLAG_FORWARD_ONLY,
        NULL,
        &amp;pEnum);

    if (FAILED(hr))
    {
        // Handle error
        goto cleanup;
    }
    
    // The query will return only one instance. 
    hr = pEnum-&gt;Next(WBEM_INFINITE, 1, &amp;pWinSAT, &amp;returned);
    if (FAILED(hr))
    {
        // Handle error
        goto cleanup;
    }
    
    hr = pWinSAT-&gt;Get(L"WinSPRLevel", 0, &amp;vBaseScore, NULL, NULL);
    if (FAILED(hr))
    {
        // Handle error
        goto cleanup;
    }

    *pBaseScore = vBaseScore.fltVal;

    hr = pWinSAT-&gt;Get(L"WinSATAssessmentState", 0, &amp;vState, NULL, NULL);
    if (FAILED(hr))
    {
        // Handle error
        goto cleanup;
    }

    *pState = (WINSAT_ASSESSMENT_STATE)vState.lVal;

cleanup:

    if (pLocator)
        pLocator-&gt;Release();

    if (pServices)
        pServices-&gt;Release();

    if (pEnum)
        pEnum-&gt;Release();

    if (pWinSAT)
        pWinSAT-&gt;Release();

    return hr;
}


HRESULT GetScoreBitmap(const float BaseScore, const WINSAT_ASSESSMENT_STATE State, HBITMAP* phbitmap)
{
    HRESULT hr = S_OK;
    IProvideWinSATVisuals* pVisuals = NULL;

    // Code to retrieve the bitmap from WinSAT. Get the bitmap
    // only if the state is one of the following states.
    if (WINSAT_ASSESSMENT_STATE_VALID == State ||
        WINSAT_ASSESSMENT_STATE_INCOHERENT_WITH_HARDWARE == State)
    {
        hr = CoCreateInstance(__uuidof(CProvideWinSATVisuals),
            NULL,
            CLSCTX_INPROC_SERVER,
            __uuidof(IProvideWinSATVisuals),
            (void**)&amp;pVisuals);

        if (FAILED(hr))
        {
            // Handle error
            goto cleanup;
        }

        hr = pVisuals-&gt;get_Bitmap(WINSAT_BITMAP_SIZE_NORMAL, 
            State, 
            BaseScore, 
            phbitmap);

        if (FAILED(hr))
        {
            // Handle error
            goto cleanup;
        }
    }

cleanup:

    if (pVisuals)
        pVisuals-&gt;Release();

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9e8d2490-9d48-4512-b5f0-5c2f9cdeb287">IProvideWinSATVisuals</a>
 

 

