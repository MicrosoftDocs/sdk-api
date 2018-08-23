---
UID: NF:uiribbon.IUIApplication.OnViewChanged
title: IUIApplication::OnViewChanged
author: windows-sdk-content
description: Called when the state of a View changes.
old-location: windowsribbon\windowsribbon_iuiapplication_onviewchanged.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiapplication\onviewchanged.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUIApplication interface [Windows Ribbon],OnViewChanged method, IUIApplication.OnViewChanged, IUIApplication::OnViewChanged, OnViewChanged, OnViewChanged method [Windows Ribbon], OnViewChanged method [Windows Ribbon],IUIApplication interface, scenicintent_IUIApplication_OnViewChanged, uiribbon/IUIApplication::OnViewChanged, windowsribbon.windowsribbon_iuiapplication_onviewchanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiribbon.h
req.include-header: 
req.redist: 
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
 - IUIApplication.OnViewChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUIApplication::OnViewChanged


## -description


Called when the state of a  <a href="https://msdn.microsoft.com/e7549b8b-0f95-477a-9024-1a99ee1412c2">View</a> changes.


## -parameters




### -param viewId [in]

Type: <b>UINT32</b>

The ID for the View. 
				Only a value of 0 is valid. 


### -param typeID [in]

Type: <b><a href="https://msdn.microsoft.com/9df0b3b7-f41b-4f0b-aa04-307b2eb7652a">UI_VIEWTYPE</a></b>

The <a href="https://msdn.microsoft.com/9df0b3b7-f41b-4f0b-aa04-307b2eb7652a">UI_VIEWTYPE</a> hosted by the application.
				


### -param view [in]

Type: <b><a href="_com_iunknown">IUnknown</a>*</b>

A pointer to the View interface.
				


### -param verb [in]

Type: <b><a href="https://msdn.microsoft.com/9245db43-1bd3-488f-b50b-c56576108109">UI_VIEWVERB</a></b>

The <a href="https://msdn.microsoft.com/9245db43-1bd3-488f-b50b-c56576108109">UI_VIEWVERB</a> (or action) performed by the View.
				


### -param uReasonCode [in]

Type: <b>INT32</b>

Not defined.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This callback notification is sent by the framework to the host application on each View state change.
			

<div class="alert"><b>Important</b>  This callback only occurs for the <a href="https://msdn.microsoft.com/51083180-4e86-4c90-9fd1-a58c12bcc756">Ribbon View</a> with a <i>viewId</i> of 0.</div>
<div> </div>
<b>IUIApplication::OnViewChanged</b> is useful for initializing Ribbon properties when the host application starts, modifying Ribbon properties based on user actions, such as resizing the application window, and querying Ribbon properties when the application closes. 


#### Examples



The following example demonstrates a basic implementation of the <b>IUIApplication::OnViewChanged</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
//  FUNCTION: OnViewChanged(UINT, UI_VIEWTYPE, IUnknown*, UI_VIEWVERB, INT)
//
//  PURPOSE: Called when the state of a View (Ribbon is a view) changes - like created/destroyed/resized.
//
//  PARAMETERS:    
//                viewId - The View identifier. 
//                typeID - The View type. 
//                pView - Pointer to the View interface. 
//                verb - The action performed by the View. 
//                uReasonCode - Not defined. 
//
//  COMMENTS:
//
//    For this sample, return the same command handler for all commands
//    specified in the .xml file.
//    
//
STDMETHODIMP CApplication::OnViewChanged(
    UINT viewId,
    UI_VIEWTYPE typeId,
    IUnknown* pView,
    UI_VIEWVERB verb,
    INT uReasonCode)
{
    HRESULT hr = E_NOTIMPL;
    
    // Checks to see if the view that was changed was a Ribbon view.
    if (UI_VIEWTYPE_RIBBON == typeId)
    {
        switch (verb)
        {            
            // The view was newly created.
            case UI_VIEWVERB_CREATE:
                _cwprintf(L"IUIApplication::OnViewChanged called with verb=CREATE\r\n");

                if (NULL == g_pRibbon)
                {
                    // Retrieve and store the IUIRibbon
                    hr = pView-&gt;QueryInterface(&amp;g_pRibbon);
                }
                break;

            // The view was resized.  
            // In the case of the Ribbon view, the application should call 
            // GetHeight() to determine the height of the Ribbon.
            case UI_VIEWVERB_SIZE:
                _cwprintf(L"IUIApplication::OnViewChanged called with verb=SIZE\r\n");
                // Call to the framework to determine the height of the Ribbon.
                if (NULL != g_pRibbon)
                {
                    UINT uRibbonHeight;
                    hr = g_pRibbon-&gt;GetHeight(&amp;uRibbonHeight);
                }
                if (!SUCCEEDED(hr))
                {
                    //_cwprintf(L"IUIRibbon::GetHeight() failed with hr=0x%X\r\n", hr);
                }
                break;
                
            // The view was destroyed.
            case UI_VIEWVERB_DESTROY:
                //_cwprintf(L"IUIApplication::OnViewChanged called with verb=DESTROY\r\n");
                g_pRibbon = NULL;
                hr = S_OK;
                break;
        }
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0df1d890-cc78-4375-a17e-6fe7c0249107">IUIApplication</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

