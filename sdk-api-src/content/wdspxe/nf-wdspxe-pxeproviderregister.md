---
UID: NF:wdspxe.PxeProviderRegister
title: PxeProviderRegister function
author: windows-sdk-content
description: Registers a provider with the system.
old-location: wds\pxeproviderregister.htm
old-project: wds
ms.assetid: 2b377855-dae7-47cb-925a-9ee0a9265f83
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PXE_REG_INDEX_BOTTOM, PXE_REG_INDEX_TOP, PxeProviderRegister, PxeProviderRegister function [Windows Deployment Services], wds.pxeproviderregister, wdspxe/PxeProviderRegister
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
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
req.typenames: WDS_CLI_CRED, *PWDS_CLI_CRED, *LPWDS_CLI_CRED
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeProviderRegister
product: Windows
targetos: Windows
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

