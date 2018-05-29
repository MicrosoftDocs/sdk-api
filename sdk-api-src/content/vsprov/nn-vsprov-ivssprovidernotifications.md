---
UID: NN:vsprov.IVssProviderNotifications
title: IVssProviderNotifications
author: windows-sdk-content
description: The IVssProviderNotifications interface manages providers registered with VSS.
old-location: base\ivssprovidernotifications.htm
old-project: VSS
ms.assetid: 09324f54-8902-43d1-a4f9-967adccbf8be
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssProviderNotifications, IVssProviderNotifications interface [VSS], IVssProviderNotifications interface [VSS],described, base.ivssprovidernotifications, vsprov/IVssProviderNotifications
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VSS_MGMT_OBJECT_UNION, *PVSS_MGMT_OBJECT_UNION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VsProv.h
api_name:
-	IVssProviderNotifications
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssProviderNotifications interface


## -description


The <b>IVssProviderNotifications</b> interface 
   manages providers registered with VSS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssProviderNotifications</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssProviderNotifications</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssProviderNotifications</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd3df604-074b-4206-827e-3cc4d5f71f87">OnLoad</a>
</td>
<td align="left" width="63%">
Notifies the provider that it was just loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b9e0940-70b4-4913-9281-0347e60baa0d">OnUnload</a>
</td>
<td align="left" width="63%">
Notifies the provider that it was just unloaded.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3a0c60df-666c-4e33-a54c-7fa5ddbfde13">Volume Shadow Copy API Interfaces</a>
 

 

