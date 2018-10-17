---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE
author: windows-sdk-content
description: Releases the provider.
old-location: security\pfn_crypt_object_locator_provider_release.htm
tech.root: seccrypto
ms.assetid: DDF1243D-A6C8-426A-A800-018E7FF7E182
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: CRYPT_OBJECT_LOCATOR_RELEASE_DLL_UNLOAD, CRYPT_OBJECT_LOCATOR_RELEASE_PROCESS_EXIT, CRYPT_OBJECT_LOCATOR_RELEASE_SERVICE_STOP, CRYPT_OBJECT_LOCATOR_RELEASE_SYSTEM_SHUTDOWN, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE callback, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE callback function [Security], security.pfn_crypt_object_locator_provider_release, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Pointer to an optional buffer defined by this provider and returned by the <a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> function. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information. 


## -returns



Do not return a value from this function. 




## -remarks



The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE</b> callback function is currently called by only the Secure Channel (Schannel) security package. This function is called once for every call made to <a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>.

The provider is not expected to release all memory for all objects but should clean itself if the <i>dwReason</i> parameter is set to <b>CRYPT_OBJECT_LOCATOR_RELEASE_SERVICE_STOP</b> or <b>CRYPT_OBJECT_LOCATOR_RELEASE_DLL_UNLOAD</b>.

This function must block so that  calls to <a href="https://msdn.microsoft.com/F6EE5424-A3ED-4E90-897B-56C605EB985C">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH</a> can complete.




## -see-also




<a href="https://msdn.microsoft.com/4B319A83-C230-4BFE-AF21-1395ED2D234B">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="https://msdn.microsoft.com/DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>
 

 

