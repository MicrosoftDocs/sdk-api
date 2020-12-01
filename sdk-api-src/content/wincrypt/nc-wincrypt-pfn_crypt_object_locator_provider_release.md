---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE (wincrypt.h)
description: Releases the provider.
helpviewer_keywords: ["CRYPT_OBJECT_LOCATOR_RELEASE_DLL_UNLOAD","CRYPT_OBJECT_LOCATOR_RELEASE_PROCESS_EXIT","CRYPT_OBJECT_LOCATOR_RELEASE_SERVICE_STOP","CRYPT_OBJECT_LOCATOR_RELEASE_SYSTEM_SHUTDOWN","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE callback","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE callback function [Security]","security.pfn_crypt_object_locator_provider_release","wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE"]
old-location: security\pfn_crypt_object_locator_provider_release.htm
tech.root: security
ms.assetid: DDF1243D-A6C8-426A-A800-018E7FF7E182
ms.date: 12/05/2018
ms.keywords: CRYPT_OBJECT_LOCATOR_RELEASE_DLL_UNLOAD, CRYPT_OBJECT_LOCATOR_RELEASE_PROCESS_EXIT, CRYPT_OBJECT_LOCATOR_RELEASE_SERVICE_STOP, CRYPT_OBJECT_LOCATOR_RELEASE_SYSTEM_SHUTDOWN, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE callback, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE callback function [Security], security.pfn_crypt_object_locator_provider_release, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE
 - wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE callback function


## -description

The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE</b> callback function releases the provider.

## -parameters

### -param dwReason [in]

Specifies the reason the provider is being released. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OBJECT_LOCATOR_RELEASE_SYSTEM_SHUTDOWN"></a><a id="crypt_object_locator_release_system_shutdown"></a><dl>
<dt><b>CRYPT_OBJECT_LOCATOR_RELEASE_SYSTEM_SHUTDOWN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The computer is shutting down.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OBJECT_LOCATOR_RELEASE_SERVICE_STOP"></a><a id="crypt_object_locator_release_service_stop"></a><dl>
<dt><b>CRYPT_OBJECT_LOCATOR_RELEASE_SERVICE_STOP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The service is stopping.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OBJECT_LOCATOR_RELEASE_PROCESS_EXIT"></a><a id="crypt_object_locator_release_process_exit"></a><dl>
<dt><b>CRYPT_OBJECT_LOCATOR_RELEASE_PROCESS_EXIT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The calling process is ending.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OBJECT_LOCATOR_RELEASE_DLL_UNLOAD"></a><a id="crypt_object_locator_release_dll_unload"></a><dl>
<dt><b>CRYPT_OBJECT_LOCATOR_RELEASE_DLL_UNLOAD</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The provider DLL is unloading.

</td>
</tr>
</table>

### -param pPluginContext [in, optional]

Pointer to an optional buffer defined by this provider and returned by the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> function. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information.

## -remarks

The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE</b> callback function is currently called by only the Secure Channel (Schannel) security package. This function is called once for every call made to <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>.

The provider is not expected to release all memory for all objects but should clean itself if the <i>dwReason</i> parameter is set to <b>CRYPT_OBJECT_LOCATOR_RELEASE_SERVICE_STOP</b> or <b>CRYPT_OBJECT_LOCATOR_RELEASE_DLL_UNLOAD</b>.

This function must block so that  calls to <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_flush">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH</a> can complete.

## -see-also

<a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_object_locator_provider_table">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>