---
UID: NF:uiribbon.IUIFramework.GetView
title: IUIFramework::GetView
author: windows-sdk-content
description: Retrieves the address of a pointer to an interface that represents a Windows Ribbon framework View, such as IUIRibbon or IUIContextualUI.
old-location: windowsribbon\windowsribbon_iuiframework_getview.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\getview.htm
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: GetView, GetView method [Windows Ribbon], GetView method [Windows Ribbon],IUIFramework interface, IUIFramework interface [Windows Ribbon],GetView method, IUIFramework.GetView, IUIFramework::GetView, scenicintent_IUIFramework_GetView, uiribbon/IUIFramework::GetView, windowsribbon.windowsribbon_iuiframework_getview
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
 - IUIFramework.GetView
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUIFramework::GetView


## -description



			Retrieves the address of a pointer to an interface that represents a Windows Ribbon framework View, such as <a href="https://msdn.microsoft.com/6a43f17b-dbf6-4c5b-818f-c0dde896de99">IUIRibbon</a> 
			or <a href="https://msdn.microsoft.com/dbefd3e0-bb47-41df-b164-b2f279380e36">IUIContextualUI</a>.
		


## -parameters




### -param viewId [in]

Type: <b>UINT32</b>


					The ID for the View. 
				A value of 0 for a <a href="https://msdn.microsoft.com/51083180-4e86-4c90-9fd1-a58c12bcc756">Ribbon</a> or the <a href="https://msdn.microsoft.com/937ca9d6-6910-4133-9cfa-d7e3f895f876">Command.Id</a> of a <a href="https://msdn.microsoft.com/b955be16-803e-47b5-a72d-f993180fbf14">ContextPopup</a>. 


### -param riid [in]

Type: <b>REFIID</b>


					The interface ID for <a href="https://msdn.microsoft.com/6a43f17b-dbf6-4c5b-818f-c0dde896de99">IUIRibbon</a> 
					or <a href="https://msdn.microsoft.com/dbefd3e0-bb47-41df-b164-b2f279380e36">IUIContextualUI</a>.
				


### -param ppv [out]

Type: <b>void**</b>


					When this method returns, contains the address of a pointer to an <a href="https://msdn.microsoft.com/6a43f17b-dbf6-4c5b-818f-c0dde896de99">IUIRibbon</a> 
					or an <a href="https://msdn.microsoft.com/dbefd3e0-bb47-41df-b164-b2f279380e36">IUIContextualUI</a> object. 
					


## -returns



Type: <b>HRESULT</b>


					Returns S_OK if successful; otherwise, an error value from the following list.
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td><i>riid</i> is not a valid interface ID.
				</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>The operation failed.</td>
</tr>
</table>
 




## -remarks




				Ribbon framework UI functionality is differentiated by Views, which are essentially built-in core frameworks, 
				such as the <a href="https://msdn.microsoft.com/51083180-4e86-4c90-9fd1-a58c12bcc756">Ribbon</a> and <a href="https://msdn.microsoft.com/b955be16-803e-47b5-a72d-f993180fbf14">ContextPopup</a>.
			


				Rather than maintaining a pointer to an interface throughout the life of an application,
				<b>IUIFramework::GetView</b> enables a host application to create a temporary interface pointer 
				and call methods as necessary. 
				

<div class="alert"><b>Note</b>  The host application must call <a href="http://go.microsoft.com/fwlink/p/?linkid=142946">IUnknown::Release</a> on the temporary interface pointer to avoid a memory leak.</div>
<div> </div>

				For example, each time there is a change to the size of the ribbon, a host application calls 
				<a href="https://msdn.microsoft.com/a029aba6-7386-4c76-813d-e475b30317b3">GetHeight</a> to adjust the size of the host client area 
				appropriately. 
				


#### Examples

The following example demonstrates how to use the <b>IUIFramework::GetView</b> method to retrieve a Ribbon View object, call the <a href="https://msdn.microsoft.com/a029aba6-7386-4c76-813d-e475b30317b3">GetHeight</a> method to retrieve the height  of the ribbon, and calculate a display location for a <a href="https://msdn.microsoft.com/c41b888a-15aa-4c47-ad73-5dc30b5fa6f9">Context Popup</a> control based on the height of the ribbon.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void GetDisplayLocation(POINT &amp;pt, HWND hWnd)
{
  if (pt.x == -1 &amp;&amp; pt.y == -1)
  {
    HRESULT hr = E_FAIL;

    // Display the menu in the upper-left corner of the client area, below the ribbon.
    IUIRibbon* pRibbon;
    hr = g_pFramework-&gt;GetView(0, IID_PPV_ARGS(&amp;pRibbon));
    if (SUCCEEDED(hr))
    {
      UINT32 uRibbonHeight = 0;
      hr = pRibbon-&gt;GetHeight(&amp;uRibbonHeight);
      if (SUCCEEDED(hr))
      {
        pt.x = 0;
        pt.y = uRibbonHeight;
        // Convert client coordinates of a specified point to screen coordinates.
        ClientToScreen(hWnd, &amp;pt);
      }
      pRibbon-&gt;Release();
    }
    if (FAILED(hr))
    {
      // Default to just the upper-right corner of the entire screen.
      pt.x = 0;
      pt.y = 0;
    }
  }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a9b8a30d-dd00-4088-a588-304fde97b84e">IUIFramework</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

