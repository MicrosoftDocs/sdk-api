---
UID: NF:uiautomationcore.IInvokeProvider.Invoke
title: IInvokeProvider::Invoke (uiautomationcore.h)
description: Sends a request to activate a control and initiate its single, unambiguous action. (IInvokeProvider.Invoke)
helpviewer_keywords: ["IInvokeProvider interface [Windows Accessibility]","Invoke method","IInvokeProvider.Invoke","IInvokeProvider::Invoke","Invoke","Invoke method [Windows Accessibility]","Invoke method [Windows Accessibility]","IInvokeProvider interface","uiauto.uiauto_IInvokeProvider_Invoke","uiauto_IInvokeProvider_Invoke","uiautomationcore/IInvokeProvider::Invoke","winauto.uiauto_IInvokeProvider_Invoke"]
old-location: winauto\uiauto_IInvokeProvider_Invoke.htm
tech.root: WinAuto
ms.assetid: 9bd2aba1-0751-412c-a6fe-0c10b9baa01e
ms.date: 12/05/2018
ms.keywords: IInvokeProvider interface [Windows Accessibility],Invoke method, IInvokeProvider.Invoke, IInvokeProvider::Invoke, Invoke, Invoke method [Windows Accessibility], Invoke method [Windows Accessibility],IInvokeProvider interface, uiauto.uiauto_IInvokeProvider_Invoke, uiauto_IInvokeProvider_Invoke, uiautomationcore/IInvokeProvider::Invoke, winauto.uiauto_IInvokeProvider_Invoke
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInvokeProvider::Invoke
 - uiautomationcore/IInvokeProvider::Invoke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IInvokeProvider.Invoke
---

# IInvokeProvider::Invoke


## -description

Sends a request to activate a control and initiate its single, unambiguous action.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IInvokeProvider::Invoke</b> is an asynchronous call and must return immediately without blocking. 
        

<div class="alert"><b>Note</b>  This is particularly critical for controls that, directly or indirectly, launch a modal dialog when invoked. 
        Any Microsoft UI Automation client that instigated the event will remain blocked until the modal dialog is closed.
        </div>
<div> </div>
<b>IInvokeProvider::Invoke</b> raises the Invoked event after the control 
			has completed its associated action, if possible. 
            

The event should be raised before servicing the Invoke request 
			in the following scenarios:
	

<ul>
<li>It is not possible or practical to wait until the action is complete.</li>
<li>The action requires user interaction.</li>
<li>The action is time-consuming and will cause the calling client to block for a significant length of time.
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iinvokeprovider">IInvokeProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
