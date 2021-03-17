---
UID: NF:raseapif.RasEapInvokeInteractiveUI
title: RasEapInvokeInteractiveUI function (raseapif.h)
description: The RAS connection manager calls the RasEapInvokeInteractiveUI function to display a dialog to obtain authentication data from the user.
helpviewer_keywords: ["RasEapInvokeInteractiveUI","RasEapInvokeInteractiveUI callback","RasEapInvokeInteractiveUI callback function [EAP]","_eap_raseapinvokeinteractiveui","eap.raseapinvokeinteractiveui","raseapif/RasEapInvokeInteractiveUI"]
old-location: eap\raseapinvokeinteractiveui.htm
tech.root: EAP
ms.assetid: 71dd40c9-acbd-4fb6-800d-d3f83a61b7b8
ms.date: 12/05/2018
ms.keywords: RasEapInvokeInteractiveUI, RasEapInvokeInteractiveUI callback, RasEapInvokeInteractiveUI callback function [EAP], _eap_raseapinvokeinteractiveui, eap.raseapinvokeinteractiveui, raseapif/RasEapInvokeInteractiveUI
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasEapInvokeInteractiveUI
 - raseapif/RasEapInvokeInteractiveUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Raseapif.h
api_name:
 - RasEapInvokeInteractiveUI
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
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_output">PPP_EAP_OUTPUT</a> structure. The RAS Connection Manager receives the 
<b>PPP_EAP_OUTPUT</b> structure as an output parameter from the 
<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a> function.

### -param dwSizeOfUIContextData [in]

Specifies the size of the context data. The authentication protocol provides the size as a member of the 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_output">PPP_EAP_OUTPUT</a> structure. The RAS Connection Manager receives the 
<b>PPP_EAP_OUTPUT</b> structure as an output parameter from the 
<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a> function.

### -param ppDataFromInteractiveUI

[out[ Pointer to a pointer variable. On successful return, this pointer variable  points to a memory buffer that contains the data obtained by the interactive UI. The interactive UI allocates this memory. RAS passes this data back to the authentication protocol in the 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_input">PPP_EAP_INPUT</a> structure, then RAS frees this memory by calling 
<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a>. 




If the interactive UI does not obtain any user-specific data, the pointer that <i>ppUserData</i> points to should be set to <b>NULL</b>.

### -param pdwSizeOfDataFromInteractiveUI [out]

Pointer to a <b>DWORD</b> variable that receives the size of the data returned from the interactive UI. If the interactive UI does not obtain any user-specific data, the <b>DWORD</b> variable should be set to zero.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>. Check the <i>ppDataFromInteractiveUI</i> and <i>lpdwSizeOfDataFromInteractiveUI</i> parameters to determine if the function returned data from the interactive UI.

If the function was not able to allocate memory for the data, the return value should be <b>ERROR_NOT_ENOUGH_MEMORY</b>.

If the function fails in some other way, the return value should be an appropriate error code from Winerror.h, Raserror.h, or Mprerror.h.

## -remarks

The DLL that implements the 
<b>RasEapInvokeInteractiveUI</b> and 
<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a> functions may support more than one authentication protocol. The <i>dwEapTypeId</i> parameter specifies the authentication protocol for which to invoke the interactive UI.

A pointer to the data returned from the interactive UI is passed back to the authentication protocol in the <b>pDataFromInteractiveUI</b> member of 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_input">PPP_EAP_INPUT</a> structure. The 
<b>PPP_EAP_INPUT</b> structure is passed as a parameter to the 
<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a> function.

The interactive user interface must support 
<a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> messages where 
<a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a>(<i>wParam</i>) equals IDCANCEL.

## -see-also

[EAP Functions](/windows/win32/eap/eap-functions)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



[Interactive User Interface](/windows/win32/eap/interactive-user-interface)



<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_input">PPP_EAP_INPUT</a>



<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_output">PPP_EAP_OUTPUT</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapfreememory">RasEapFreeMemory</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetidentity">RasEapGetIdentity</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapinvokeconfigui">RasEapInvokeConfigUI</a>



<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a>