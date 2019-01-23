---
UID: NF:syncregistration.ISyncProviderConfigUI.ModifySyncProvider
title: ISyncProviderConfigUI::ModifySyncProvider
author: windows-sdk-content
description: Updates the ISyncProviderInfo of the synchronization provider that is configured by this ISyncProviderConfigUI.
old-location: winsync\isyncproviderconfigui_modifysyncprovider.htm
tech.root: winsync
ms.assetid: 16f6d30c-422a-4638-a63b-f9d2a5fdb8b4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncProviderConfigUI interface [Windows Sync],ModifySyncProvider method, ISyncProviderConfigUI.ModifySyncProvider, ISyncProviderConfigUI::ModifySyncProvider, ModifySyncProvider, ModifySyncProvider method [Windows Sync], ModifySyncProvider method [Windows Sync],ISyncProviderConfigUI interface, syncregistration/ISyncProviderConfigUI::ModifySyncProvider, winsync.isyncproviderconfigui_modifysyncprovider
ms.topic: method
req.header: syncregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderConfigUI.ModifySyncProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncProviderConfigUI::ModifySyncProvider


## -description


Updates the <a href="https://msdn.microsoft.com/fe50e34c-6499-4c1e-b891-7b4f797510f2">ISyncProviderInfo</a> of the synchronization provider that is configured by this <b>ISyncProviderConfigUI</b>.


## -parameters




### -param hwndParent [in]

HWND serving as the parent for the configuration UI that needs to be presented before the synchronization provider can be created. 
    	The HWND should be <b>NULL</b> only if the <b>dwCapabilities</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Dd317251(v=VS.85).aspx">SyncProviderConfigUIConfiguration</a> structure is set to not support a UI.


### -param pUnkContext [in]

Pointer to an interface containing additional information needed to generate the synchronization provider. The pointer will be <b>NULL</b> if no additional information is needed.


### -param pProviderInfo [in]

An <a href="https://msdn.microsoft.com/fe50e34c-6499-4c1e-b891-7b4f797510f2">ISyncProviderInfo</a> that provides information about the synchronization provider that is being modified.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/27757aa1-a42d-4f66-99a8-bf66385fbec1">ISyncProviderConfigUI Interface</a>
 

 

