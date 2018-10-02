---
UID: NF:eaphostpeerconfigapis.EapHostPeerInvokeConfigUI
title: EapHostPeerInvokeConfigUI function
author: windows-sdk-content
description: Starts the configuration user interface of the specified EAP method.
old-location: eaphost\eaphostpeerinvokeconfigui.htm
tech.root: EAPHost
ms.assetid: afb20482-a439-437d-9c8f-c4e87e440113
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EapHostPeerInvokeConfigUI, EapHostPeerInvokeConfigUI function [EAPHost], eaphost.eaphostpeerinvokeconfigui, eaphostpeerconfigapis/EapHostPeerInvokeConfigUI
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
 - EapHostPeerInvokeConfigUI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapHostPeerInvokeConfigUI function


## -description


Starts the configuration user interface of the specified EAP method.

<b>EapHostPeerInvokeConfigUI</b> must be called on threads that have COM initialized for <a href="Http://go.microsoft.com/fwlink/p/?linkid=83881">Single Threaded Apartment</a> (STA). This can be achieved by calling COM API <a href="_com_CoInitialize">CoInitialize</a>; when the supplicant has finished  with the STA thread <a href="_com_CoUninitialize">CoUninitialize</a> must be called before exiting.


## -parameters




### -param hwndParent [in]

The handle of the parent window under which configuration dialog appears.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param eapMethodType [in]

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that specifies the EAP method.


### -param dwSizeOfConfigIn [in]

The size of input configuration. May be set to 0 (zero).


### -param pConfigIn [in]

A pointer to a byte buffer that contains configuration elements. The buffer is of size <i>dwSizeOfConfigIn</i>. This parameter can be <b>NULL</b>, if <i>dwSizeOfConfigIn</i> is set to 0 (zero). 


### -param pdwSizeOfConfigOut [out]

A pointer to a DWORD that specifies the size of the buffer pointed to by <i>ppConfigOut</i>.


### -param ppConfigOut [out]

A pointer to a pointer to a byte buffer that contains updated configuration data from the user. After consuming the data, this memory must be freed by calling <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>.


## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>
 

 

