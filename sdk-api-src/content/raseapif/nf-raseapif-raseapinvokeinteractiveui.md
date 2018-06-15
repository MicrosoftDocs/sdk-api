---
UID: NF:raseapif.RasEapInvokeInteractiveUI
title: RasEapInvokeInteractiveUI function
author: windows-sdk-content
description: The RAS connection manager calls the RasEapInvokeInteractiveUI function to display a dialog to obtain authentication data from the user.
old-location: eap\raseapinvokeinteractiveui.htm
old-project: EAP
ms.assetid: 71dd40c9-acbd-4fb6-800d-d3f83a61b7b8
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: RasEapInvokeInteractiveUI, RasEapInvokeInteractiveUI callback, RasEapInvokeInteractiveUI callback function [EAP], _eap_raseapinvokeinteractiveui, eap.raseapinvokeinteractiveui, raseapif/RasEapInvokeInteractiveUI
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: raseapif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: RAS_AUTH_ATTRIBUTE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Raseapif.h
api_name:
 - RasEapInvokeInteractiveUI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RasEapInvokeInteractiveUI function


## -description


The RAS connection manager calls the 
<b>RasEapInvokeInteractiveUI</b> function to display a dialog to obtain authentication data from the user.


## -parameters




### -param dwEapTypeId [in]

Specifies the authentication protocol for which to invoke the interactive UI.


### -param hwndParent [in]

Handle to the parent window for the dialog.


### -param pUIContextData [in]

Pointer to context data for the interactive UI. The authentication protocol provides a pointer to this data as a member of the 
<a href="https://msdn.microsoft.com/d1634973-f6af-4be3-914a-513098c5fccf">PPP_EAP_OUTPUT</a> structure. The RAS Connection Manager receives the 
<b>PPP_EAP_OUTPUT</b> structure as an output parameter from the 
<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a> function.


### -param dwSizeOfUIContextData

TBD


### -param ppDataFromInteractiveUI

[out[ Pointer to a pointer variable. On successful return, this pointer variable  points to a memory buffer that contains the data obtained by the interactive UI. The interactive UI allocates this memory. RAS passes this data back to the authentication protocol in the 
<a href="https://msdn.microsoft.com/80a8f118-323d-4040-91f7-202eeee6d227">PPP_EAP_INPUT</a> structure, then RAS frees this memory by calling 
<a href="https://msdn.microsoft.com/d6eb6afd-0d92-4050-b6a9-7bd90788e01c">RasEapFreeMemory</a>. 




If the interactive UI does not obtain any user-specific data, the pointer that <i>ppUserData</i> points to should be set to <b>NULL</b>.


### -param pdwSizeOfDataFromInteractiveUI [out]

Pointer to a <b>DWORD</b> variable that receives the size of the data returned from the interactive UI. If the interactive UI does not obtain any user-specific data, the <b>DWORD</b> variable should be set to zero.


#### - dwSizeofUIContextData [in]

Specifies the size of the context data. The authentication protocol provides the size as a member of the 
<a href="https://msdn.microsoft.com/d1634973-f6af-4be3-914a-513098c5fccf">PPP_EAP_OUTPUT</a> structure. The RAS Connection Manager receives the 
<b>PPP_EAP_OUTPUT</b> structure as an output parameter from the 
<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a> function.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>. Check the <i>ppDataFromInteractiveUI</i> and <i>lpdwSizeOfDataFromInteractiveUI</i> parameters to determine if the function returned data from the interactive UI.

If the function was not able to allocate memory for the data, the return value should be <b>ERROR_NOT_ENOUGH_MEMORY</b>.

If the function fails in some other way, the return value should be an appropriate error code from Winerror.h, Raserror.h, or Mprerror.h.




## -remarks



The DLL that implements the 
<b>RasEapInvokeInteractiveUI</b> and 
<a href="https://msdn.microsoft.com/d6eb6afd-0d92-4050-b6a9-7bd90788e01c">RasEapFreeMemory</a> functions may support more than one authentication protocol. The <i>dwEapTypeId</i> parameter specifies the authentication protocol for which to invoke the interactive UI.

A pointer to the data returned from the interactive UI is passed back to the authentication protocol in the <b>pDataFromInteractiveUI</b> member of 
<a href="https://msdn.microsoft.com/80a8f118-323d-4040-91f7-202eeee6d227">PPP_EAP_INPUT</a> structure. The 
<b>PPP_EAP_INPUT</b> structure is passed as a parameter to the 
<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a> function.

The interactive user interface must support 
<a href="https://www.bing.com/search?q=WM_COMMAND">WM_COMMAND</a> messages where 
<a href="https://www.bing.com/search?q=LOWORD">LOWORD</a>(<i>wParam</i>) equals IDCANCEL.




## -see-also




<a href="https://msdn.microsoft.com/090a3620-3732-4466-95ac-ce9cbdd36484">EAP Functions</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/4f8ba0a4-3b52-4e7c-9e67-748f8d81d7a2">Interactive User Interface</a>



<a href="https://msdn.microsoft.com/80a8f118-323d-4040-91f7-202eeee6d227">PPP_EAP_INPUT</a>



<a href="https://msdn.microsoft.com/d1634973-f6af-4be3-914a-513098c5fccf">PPP_EAP_OUTPUT</a>



<a href="https://msdn.microsoft.com/d6eb6afd-0d92-4050-b6a9-7bd90788e01c">RasEapFreeMemory</a>



<a href="https://msdn.microsoft.com/66bc34d2-54b9-46eb-b952-6ad66868c8ce">RasEapGetIdentity</a>



<a href="https://msdn.microsoft.com/cdd9b081-e654-445e-9383-3665258f5cfa">RasEapInvokeConfigUI</a>



<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>
 

 

