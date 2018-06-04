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

# PxeProviderRegister function


## -description


Registers a provider with the system. Providers use this function during installation to 
    register with the system. On successful registration, a registry key handle is returned that should be used to 
    store configuration information.


## -parameters




### -param pszProviderName [in]

Address of a null terminated string that specifies the display name of the provider. This name is 
      displayed to the user and must be unique among registered providers.


### -param pszModulePath [in]

Address of a null-terminated string that specifies the full path to the provider DLL.


### -param Index [in]

Index into the list of providers. Any existing providers are shifted down if necessary. The administrator 
      can rearrange the providers as needed, so no assumptions should be made about the order of providers.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_REG_INDEX_TOP"></a><a id="pxe_reg_index_top"></a><dl>
<dt><b>PXE_REG_INDEX_TOP</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Add the provider to the top of the list to be the first to receive client requests.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_REG_INDEX_BOTTOM"></a><a id="pxe_reg_index_bottom"></a><dl>
<dt><b>PXE_REG_INDEX_BOTTOM</b></dt>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
Add the provider to the bottom of the list.

</td>
</tr>
</table>
 


### -param bIsCritical [in]

Indicates whether the provider is critical. If a critical provider fails, the WDS server will also 
      fail.


### -param phProviderKey [out]

Address of a <b>HKEY</b> where the configuration should be stored. The provider will 
      receive a handle to this same key as the <i>hProviderKey</i> parameter to its 
      <a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a> callback.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/433b051c-9fde-4589-92e2-58d3774826ac">PxeProviderInitialize</a>



<a href="https://msdn.microsoft.com/b468d865-c680-4f72-a10c-3d91542df8d3">PxeProviderUnRegister</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

