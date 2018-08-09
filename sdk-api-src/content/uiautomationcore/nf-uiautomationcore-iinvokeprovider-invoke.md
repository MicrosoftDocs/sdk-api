---
UID: NF:uiautomationcore.IInvokeProvider.Invoke
title: IInvokeProvider::Invoke
author: windows-sdk-content
description: Sends a request to activate a control and initiate its single, unambiguous action.
old-location: winauto\uiauto_IInvokeProvider_Invoke.htm
old-project: WinAuto
ms.assetid: 9bd2aba1-0751-412c-a6fe-0c10b9baa01e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IInvokeProvider interface [Windows Accessibility],Invoke method, IInvokeProvider.Invoke, IInvokeProvider::Invoke, Invoke, Invoke method [Windows Accessibility], Invoke method [Windows Accessibility],IInvokeProvider interface, uiauto.uiauto_IInvokeProvider_Invoke, uiauto_IInvokeProvider_Invoke, uiautomationcore/IInvokeProvider::Invoke, winauto.uiauto_IInvokeProvider_Invoke
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IInvokeProvider.Invoke
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IInvokeProvider::Invoke


## -description


Sends a request to activate a control and initiate its single, unambiguous action.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




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




<a href="https://msdn.microsoft.com/e522b8d5-c6f6-4f71-a8c8-4332f2824f72">IInvokeProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

