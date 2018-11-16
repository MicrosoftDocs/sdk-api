---
UID: NF:syncregistration.ISyncProviderConfigUI.GetRegisteredProperties
title: ISyncProviderConfigUI::GetRegisteredProperties
author: windows-sdk-content
description: Obtains configuration UI properties for reading and writing.
old-location: winsync\isyncproviderconfigui_getregisteredproperties.htm
tech.root: winsync
ms.assetid: c96091d7-4b80-445b-911a-fde612eafce9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetRegisteredProperties, GetRegisteredProperties method [Windows Sync], GetRegisteredProperties method [Windows Sync],ISyncProviderConfigUI interface, ISyncProviderConfigUI interface [Windows Sync],GetRegisteredProperties method, ISyncProviderConfigUI.GetRegisteredProperties, ISyncProviderConfigUI::GetRegisteredProperties, syncregistration/ISyncProviderConfigUI::GetRegisteredProperties, winsync.isyncproviderconfigui_getregisteredproperties
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISyncProviderConfigUI.GetRegisteredProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- syncregistration.h
: 
- ISyncProviderConfigUI.GetRegisteredProperties
: 
---

# ISyncProviderConfigUI::GetRegisteredProperties


## -description


Obtains configuration UI properties for reading and writing.


## -parameters




### -param ppConfigUIProperties [out]

Returns the <b>IPropertyStore</b> object that contains the configuration UI properties for reading and writing. Both the <a href="https://msdn.microsoft.com/fe50e34c-6499-4c1e-b891-7b4f797510f2">ISyncProviderInfo</a> and <a href="https://msdn.microsoft.com/b7c49533-d289-44b0-9a9e-cfa47af3a087">ISyncProviderConfigUIInfo</a> interfaces inherit from <b>IPropertyStore</b>.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/27757aa1-a42d-4f66-99a8-bf66385fbec1">ISyncProviderConfigUI Interface</a>
 

 

