---
UID: NF:raseapif.RasEapFreeMemory
title: RasEapFreeMemory function (raseapif.h)
description: The RAS connection manager calls RasEapFreeMemory to free memory buffers returned by RasEapInvokeConfigUI, RasEapGetIdentity, and RasEapInvokeInteractiveUI.
helpviewer_keywords: ["RasEapFreeMemory","RasEapFreeMemory callback","RasEapFreeMemory callback function [EAP]","_eap_raseapfreememory","eap.raseapfreememory","raseapif/RasEapFreeMemory"]
old-location: eap\raseapfreememory.htm
tech.root: EAP
ms.assetid: d6eb6afd-0d92-4050-b6a9-7bd90788e01c
ms.date: 12/05/2018
ms.keywords: RasEapFreeMemory, RasEapFreeMemory callback, RasEapFreeMemory callback function [EAP], _eap_raseapfreememory, eap.raseapfreememory, raseapif/RasEapFreeMemory
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
 - RasEapFreeMemory
 - raseapif/RasEapFreeMemory
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
 - RasEapFreeMemory
---

# RasEapFreeMemory function


## -description

The RAS connection manager calls 
<b>RasEapFreeMemory</b> to free memory buffers returned by 
<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapinvokeconfigui">RasEapInvokeConfigUI</a>, 
<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetidentity">RasEapGetIdentity</a>, and 
<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapinvokeinteractiveui">RasEapInvokeInteractiveUI</a>.

## -parameters

### -param pMemory [in]

Pointer to the memory to free.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value should be an appropriate error code from Winerror.h, Raserror.h, or Mprerror.h.

## -remarks

An authentication protocol may implement its various user interfaces in different DLLs. In such a case, each DLL must implement the 
<b>RasEapFreeMemory</b> function.

It is also possible that a single DLL may implement multiple user interfaces. For example, a single DLL may implement both the configuration and identity user interface for an authentication protocol. Another example would be a DLL that implements two configuration user interfaces, each to support a different authentication protocol. In these cases, the DLL must implement a single version of 
<b>RasEapFreeMemory</b> that can free memory returned from any of the user interfaces implemented in the DLL.

## -see-also

[EAP Functions](/windows/win32/eap/eap-functions)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetidentity">RasEapGetIdentity</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapinvokeconfigui">RasEapInvokeConfigUI</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapinvokeinteractiveui">RasEapInvokeInteractiveUI</a>