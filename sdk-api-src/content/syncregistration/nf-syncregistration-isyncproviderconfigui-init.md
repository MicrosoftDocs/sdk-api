---
UID: NF:syncregistration.ISyncProviderConfigUI.Init
title: ISyncProviderConfigUI::Init
author: windows-sdk-content
description: Initializes the configuration UI for a synchronization provider.
old-location: winsync\isyncproviderconfigui_init.htm
old-project: winsync
ms.assetid: c4705bc9-c5ab-46f9-ace8-7e96c16dfb75
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISyncProviderConfigUI interface [Windows Sync],Init method, ISyncProviderConfigUI.Init, ISyncProviderConfigUI::Init, Init, Init method [Windows Sync], Init method [Windows Sync],ISyncProviderConfigUI interface, syncregistration/ISyncProviderConfigUI::Init, winsync.isyncproviderconfigui_init
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNC_REGISTRATION_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderConfigUI.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncProviderConfigUI::Init


## -description


Initializes the configuration UI for a synchronization provider.


## -parameters




### -param pguidInstanceId [in]

The instance ID of the configuration UI.


### -param pguidContentType [in]

A GUID that represents the content type that is associated with the synchronization provider that this configuration UI will create.


### -param pConfigurationProperties [in]

The properties that should be specified when the configuration UI is registering the synchronization provider. These properties are also used to  properly initialize
        the configuration UI object.


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
 




## -remarks



This method will be called by the registration code before the object is returned whenever an instance of the configuration UI is requested from one of the registration interfaces.




## -see-also




<a href="https://msdn.microsoft.com/27757aa1-a42d-4f66-99a8-bf66385fbec1">ISyncProviderConfigUI Interface</a>
 

 

