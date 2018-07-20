---
UID: NF:uiribbon.IUIFramework.LoadUI
title: IUIFramework::LoadUI
author: windows-sdk-content
description: Loads the Windows Ribbon framework UI resource, or compiled markup, file.
old-location: windowsribbon\windowsribbon_iuiframework_loadui.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\loadui.htm
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IUIFramework interface [Windows Ribbon],LoadUI method, IUIFramework.LoadUI, IUIFramework::LoadUI, LoadUI, LoadUI method [Windows Ribbon], LoadUI method [Windows Ribbon],IUIFramework interface, scenicintent_IUIFramework_LoadUI, uiribbon/IUIFramework::LoadUI, windowsribbon.windowsribbon_iuiframework_loadui
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UI_VIEWVERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIFramework.LoadUI
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUIFramework::LoadUI


## -description



			Loads the Windows Ribbon framework UI resource, or compiled markup, file.
		


## -parameters




### -param instance [in]

Type: <b>HINSTANCE</b>


					A handle to the Ribbon application instance. 
				


### -param resourceName [in]

Type: <b>LPCWSTR</b>


					The name of the resource that contains the compiled, binary markup.
				

<div class="alert"><b>Note</b>  To initialize the Ribbon successfully, a compiled Ribbon markup file must be available as a resource. This markup file is an integral component of the Ribbon framework; it specifies the controls to use and their layout.
			</div>
<div> </div>

## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IUIFramework::LoadUI</b> should be called upon initialization. This method can be called multiple times during the lifecycle of an application, for example, to show or hide a Ribbon, provided that <a href="https://msdn.microsoft.com/library/Dd371368(v=VS.85).aspx">IUIFramework::Destroy</a> is called in between. 
			


<a href="https://msdn.microsoft.com/library/Dd371531(v=VS.85).aspx">OnCreateUICommand</a> and <a href="https://msdn.microsoft.com/library/Dd371537(v=VS.85).aspx">OnViewChanged</a> 
				are called during the execution of <b>IUIFramework::LoadUI</b>.
			


#### Examples



The following example demonstrates a basic framework initialization function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
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
        IID_PPV_ARGS(&amp;g_pFramework));
    if (!SUCCEEDED(hr))
    {
        return false;
    }    

    // Create the application object (IUIApplication) and call the 
    // framework Initialize method, passing the application object and the 
    // host HWND that the Ribbon will attach itself to.
    CComObject&lt;CApplication&gt; *pApplication = NULL;
    CComObject&lt;CApplication&gt;::CreateInstance(&amp;pApplication);
    hr = pApplication-&gt;QueryInterface(&amp;g_pApplication);
    if (!SUCCEEDED(hr))
    {
        return false;
    } 

    hr = g_pFramework-&gt;Initialize(hWnd, g_pApplication);
    if (!SUCCEEDED(hr))
    {
        return false;
    }

    // Load the binary markup.  
    // Initiate callbacks to the IUIApplication object that was 
    // provided to the framework earlier and bind command handler(s) 
    // to individual commands.
    hr = g_pFramework-&gt;LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (!SUCCEEDED(hr))
    {
        return false;
    }
    return true;
}
</pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/Dd316930(v=VS.85).aspx">Compiling Ribbon Markup</a>



<a href="https://msdn.microsoft.com/library/Dd371467(v=VS.85).aspx">IUIFramework</a>



<a href="https://msdn.microsoft.com/library/Dd371373(v=VS.85).aspx">IUIFramework::Initialize</a>



<a href="https://msdn.microsoft.com/library/Dd371591(v=VS.85).aspx">Markup Elements</a>



<a href="https://msdn.microsoft.com/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 

