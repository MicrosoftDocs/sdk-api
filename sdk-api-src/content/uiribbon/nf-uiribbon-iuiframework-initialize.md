---
UID: NF:uiribbon.IUIFramework.Initialize
title: IUIFramework::Initialize (uiribbon.h)
description: Connects the host application to the Windows Ribbon framework.
helpviewer_keywords: ["IUIFramework interface [Windows Ribbon]","Initialize method","IUIFramework.Initialize","IUIFramework::Initialize","Initialize","Initialize method [Windows Ribbon]","Initialize method [Windows Ribbon]","IUIFramework interface","scenicintent_IUIFramework_Initialize","uiribbon/IUIFramework::Initialize","windowsribbon.windowsribbon_iuiframework_initialize"]
old-location: windowsribbon\windowsribbon_iuiframework_initialize.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\initialize.htm
ms.date: 12/05/2018
ms.keywords: IUIFramework interface [Windows Ribbon],Initialize method, IUIFramework.Initialize, IUIFramework::Initialize, Initialize, Initialize method [Windows Ribbon], Initialize method [Windows Ribbon],IUIFramework interface, scenicintent_IUIFramework_Initialize, uiribbon/IUIFramework::Initialize, windowsribbon.windowsribbon_iuiframework_initialize
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mshtml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
f1_keywords:
 - IUIFramework::Initialize
 - uiribbon/IUIFramework::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIFramework.Initialize
---

# IUIFramework::Initialize


## -description

Connects the host application to the Windows Ribbon framework.

## -parameters

### -param frameWnd [in]

Type: <b>HWND</b>

Handle to the top-level window that will contain the Ribbon.

### -param application [in]

Type: <b><a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication">IUIApplication</a>*</b>

Pointer to the IUIApplication implementation of the host application.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful; otherwise, an error value from the following list.
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_INVALID_WINDOW_HANDLE)</td>
<td><i>frameWnd</i> is <b>NULL</b>, does not point to an existing window, or is not a top-level window of the desktop.
				<div class="alert"><b>Note</b>  This error is also returned if <i>frameWnd</i> is a child window (WS_CHILD), is declared as a tool window (WS_EX_TOOLWINDOW), or it lacks a caption property (WS_CAPTION is mandatory).</div>
<div> </div>
</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_WINDOW_OF_OTHER_THREAD)</td>
<td><i>frameWnd</i> is not owned by the execution thread.</td>
</tr>
<tr>
<td>E_POINTER</td>
<td><i>application</i> is <b>NULL</b> or an invalid pointer.</td>
</tr>
</table>

## -remarks

This method must be called by the host application for each top-level window that requires a ribbon.
			

This method is used to set up the hooks that enable the Ribbon framework to invoke callbacks in the host application.

To initialize the Ribbon successfully, a compiled Ribbon markup file must be available as a resource and specified in a subsequent call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui">IUIFramework::LoadUI</a>. This markup file is an integral component of the framework; it specifies the controls to be used and their layout.

If <b>IUIFramework::Initialize</b> returns successfully: 

<ul>
<li>To eliminate inconsistency, redundancy, and incompatibility between Ribbon and traditional command models, the Ribbon framework removes  the standard menu bar of the top-level window in the host application.</li>
<li>The framework removes references to the WS_EX_CLIENTEDGE style. <div class="alert"><b>Note</b>  The WS_EX_CLIENTEDGE style specifies that a window has a border with a sunken edge. This style visually interferes with the integration of the Ribbon and the host application.</div>
<div> </div>
</li>
<li>The framework requires that the WS_SYSMENU style be enabled. If WS_SYSMENU is not enabled, the framework does not provide alternate functionality and unpredictable rendering of the Ribbon may result.<div class="alert"><b>Note</b>  The WS_SYSMENU style specifies that the application window has a system menu on its title bar. By association, the WS_CAPTION style must also be specified (see ERROR_INVALID_WINDOW_HANDLE in <b>Return Values</b> above).</div>
<div> </div>
</li>
</ul>

#### Examples



The following example demonstrates a basic framework initialization function.


```cpp
//
//  FUNCTION:    InitializeFramework(HWND)
//
//  PURPOSE:    Initialize the Ribbon framework and bind a Ribbon to the application.
//
//  PARAMETERS:    
//                hWnd - Handle to the Ribbon host application window. 
//
//  COMMENTS:
//
//    In order to get a Ribbon to display, the Ribbon framework must be initialized. 
//    This involves three important steps:
//      1) Instantiate the Ribbon framework object (CLSID_UIRibbonFramework).
//      2) Pass the host HWND and IUIApplication object to the framework.
//      3) Load the binary markup compiled by the UI Command Compiler (UICC.exe).
//
//
bool InitializeFramework(HWND hWnd)
{
    // Instantiate the Ribbon framework object.
    HRESULT hr = CoCreateInstance(
        CLSID_UIRibbonFramework, 
        NULL, 
        CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&g_pFramework));
    if (!SUCCEEDED(hr))
    {
        return false;
    }    

    // Create the application object (IUIApplication) and call the 
    // framework Initialize method, passing the application object and the 
    // host HWND that the Ribbon will attach itself to.
    CComObject<CApplication> *pApplication = NULL;
    CComObject<CApplication>::CreateInstance(&pApplication);
    hr = pApplication->QueryInterface(&g_pApplication);
    if (!SUCCEEDED(hr))
    {
        return false;
    } 

    hr = g_pFramework->Initialize(hWnd, g_pApplication);
    if (!SUCCEEDED(hr))
    {
        return false;
    }

    // Load the binary markup.  
    // Initiate callbacks to the IUIApplication object that was 
    // provided to the framework earlier and bind command handler(s) 
    // to individual commands.
    hr = g_pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (!SUCCEEDED(hr))
    {
        return false;
    }
    return true;
}

```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework">IUIFramework</a>



<a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui">IUIFramework::LoadUI</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-reference-markup-elements">Markup Elements</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>