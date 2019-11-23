---
UID: NF:syncregistration.ISyncProviderConfigUI.GetRegisteredProperties
title: ISyncProviderConfigUI::GetRegisteredProperties (syncregistration.h)

description: Obtains configuration UI properties for reading and writing.
old-location: winsync\isyncproviderconfigui_getregisteredproperties.htm
tech.root: winsync
ms.assetid: c96091d7-4b80-445b-911a-fde612eafce9

ms.date: 12/05/2018
ms.keywords: GetRegisteredProperties, GetRegisteredProperties method [Windows Sync], GetRegisteredProperties method [Windows Sync],ISyncProviderConfigUI interface, ISyncProviderConfigUI interface [Windows Sync],GetRegisteredProperties method, ISyncProviderConfigUI.GetRegisteredProperties, ISyncProviderConfigUI::GetRegisteredProperties, syncregistration/ISyncProviderConfigUI::GetRegisteredProperties, winsync.isyncproviderconfigui_getregisteredproperties
ms.topic: method
f1_keywords: 
 - "syncregistration/ISyncProviderConfigUI.GetRegisteredProperties"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncProviderConfigUI::GetRegisteredProperties


## -description


Obtains configuration UI properties for reading and writing.


## -parameters




### -param ppConfigUIProperties [out]

Returns the <b>IPropertyStore</b> object that contains the configuration UI properties for reading and writing. Both the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderinfo">ISyncProviderInfo</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfiguiinfo">ISyncProviderConfigUIInfo</a> interfaces inherit from <b>IPropertyStore</b>.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderconfigui">ISyncProviderConfigUI Interface</a>
 

 

