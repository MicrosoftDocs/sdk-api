---
UID: NF:eaphostpeerconfigapis.EapHostPeerInvokeInteractiveUI
title: EapHostPeerInvokeInteractiveUI function
author: windows-sdk-content
description: Raises an interactive user interface used to get credentials from the user.
old-location: eaphost\eaphostpeerinvokeinteractiveui.htm
tech.root: EAPHost
ms.assetid: a4a46b77-f8ab-4062-b966-1590ea9e46d2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EapHostPeerInvokeInteractiveUI, EapHostPeerInvokeInteractiveUI function [EAPHost], eaphost.eaphostpeerinvokeinteractiveui, eaphostpeerconfigapis/EapHostPeerInvokeInteractiveUI
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: eaphostpeerconfigapis.h
req.include-header: 
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
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerInvokeInteractiveUI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapHostPeerInvokeInteractiveUI function


## -description


Raises an interactive user interface used to get credentials from the user. For example, this function can be used to raise a UI that retrieves credentials from a smart card, and prompts the user to enter the corresponding PIN.

<b>EapHostPeerInvokeInteractiveUI</b> must be called on threads that have COM initialized for <a href="Http://go.microsoft.com/fwlink/p/?linkid=83881">Single Threaded Apartment</a>. This can be achieved by calling COM API <a href="_com_CoInitialize">CoInitialize</a>; when the supplicant has finished  with the STA thread <a href="_com_CoUninitialize">CoUninitialize</a> must be called before exiting.


## -parameters




### -param hwndParent [in]

The handle of the parent window under which configuration dialog appears.


### -param dwSizeofUIContextData [in]

The size, in bytes, of the buffer pointed to by the <i>pUIContextData</i> parameter.


### -param pUIContextData [in]

A pointer to a buffer that contains the supplicant UI context data from EAPHost. The context data is returned by  <a href="https://msdn.microsoft.com/47ade6f1-067b-48ab-b4ac-a3d3cf63d809">EapHostPeerGetUIContext</a>. The buffer  is of size <i>dwSizeOfUIContextData</i>.


### -param pdwSizeOfDataFromInteractiveUI [out]

A pointer to a DWORD  that represents the size, in bytes, of the buffer pointed to by the <i>ppDataFromInteractiveUI</i> parameter.


### -param ppDataFromInteractiveUI [out]

A pointer to a pointer to a byte buffer that  contains data from the interactive UI necessary for authentication to continue. The parameter <i>ppDataFromInteractiveUI</i> should be passed to <a href="https://msdn.microsoft.com/f532dd65-d807-4880-9339-ba233e0faa38">EapHostPeerSetUIContext</a> as the IN parameter <i>pUIContextData</i>. After consuming the data, this memory must be freed by calling <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>. The buffer is of size <i>pdwSizeofDataFromInteractiveUI</i>. 


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>.


## -remarks



The supplicant should call <a href="https://msdn.microsoft.com/facf4ccf-c2e3-435e-8333-8d2c5bbe0186">EapHostPeerQueryInteractiveUIInputFields</a> function first after receiving the <a href="https://msdn.microsoft.com/59bf6e02-90b5-4f9a-9865-b71852c61db9">EapHostPeerResponseInvokeUI</a> action code from EAPHost. If <a href="https://msdn.microsoft.com/081b7a72-abe3-4cbb-9b6c-07bb6717fbfe">EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED</a> is returned, the supplicant should resort to the traditional model of invoking method interactive UI by calling <b>EapHostPeerInvokeInteractiveUI</b>. 

If called,<b>EapHostPeerInvokeInteractiveUI</b> raises the user interface for the EAP method after the supplicant calls <a href="https://msdn.microsoft.com/47ade6f1-067b-48ab-b4ac-a3d3cf63d809">EapHostPeerGetUIContext</a>. This occurs when a call to <a href="https://msdn.microsoft.com/7b3bc23d-312d-494d-afd0-ce82d2d5136c">EapHostPeerProcessReceivedPacket</a> 
   returns the <b>EapHostPeerResponseInvokeUi</b>action code. <b>EapHostPeerGetUIContext</b>returns UI context that 
   the supplicant then passes to <b>EapHostPeerInvokeInteractiveUI</b> to raise the UI.




## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/47ade6f1-067b-48ab-b4ac-a3d3cf63d809">EapHostPeerGetUIContext</a>



<a href="https://msdn.microsoft.com/facf4ccf-c2e3-435e-8333-8d2c5bbe0186">EapHostPeerQueryInteractiveUIInputFields</a>



<a href="https://msdn.microsoft.com/f532dd65-d807-4880-9339-ba233e0faa38">EapHostPeerSetUIContext</a>
 

 

