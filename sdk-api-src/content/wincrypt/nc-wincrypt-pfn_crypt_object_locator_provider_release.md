---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

