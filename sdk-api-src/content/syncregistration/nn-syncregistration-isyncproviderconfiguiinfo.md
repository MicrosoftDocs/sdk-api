---
UID: NN:syncregistration.ISyncProviderConfigUIInfo
title: ISyncProviderConfigUIInfo
author: windows-sdk-content
description: Represents the information and properties needed to create an instance of a synchronization provider configuration UI.
old-location: winsync\isyncproviderconfiguiinfo.htm
tech.root: winsync
ms.assetid: b7c49533-d289-44b0-9a9e-cfa47af3a087
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISyncProviderConfigUIInfo, ISyncProviderConfigUIInfo interface [Windows Sync], ISyncProviderConfigUIInfo interface [Windows Sync],described, syncregistration/ISyncProviderConfigUIInfo, winsync.isyncproviderconfiguiinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ISyncProviderConfigUIInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncProviderConfigUIInfo interface


## -description


Represents the information and properties needed to create an instance of a synchronization provider configuration UI.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncProviderConfigUIInfo</b> interface inherits from <b>IPropertyStore</b>. <b>ISyncProviderConfigUIInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncProviderConfigUIInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb9a2f2f-4c9f-405c-90f6-b251ab1a652d">GetSyncProviderConfigUI</a>
</td>
<td align="left" width="63%">
Creates an instance of a synchronization provider configuration UI.

</td>
</tr>
</table> 


## -remarks



You can get and set the properties of a  synchronization provider configuration UI by calling the <a href="https://msdn.microsoft.com/eb9a2f2f-4c9f-405c-90f6-b251ab1a652d">GetSyncProviderConfigUI</a>method and manipulating the configuration UI's <b>IPropertyStore</b>.




## -see-also




<a href="https://msdn.microsoft.com/8233671e-bf89-448d-8347-9b4f0ae7501f">Windows Sync Registration Reference</a>
 

 

