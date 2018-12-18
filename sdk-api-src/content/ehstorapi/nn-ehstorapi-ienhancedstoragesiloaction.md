---
UID: NN:ehstorapi.IEnhancedStorageSiloAction
title: IEnhancedStorageSiloAction
author: windows-sdk-content
description: Use this interface as a point of access for actions involving IEEE 1667 silos.
old-location: enstor\ienhancedstoragesiloaction.htm
tech.root: enstor
ms.assetid: 6deb7e22-f153-45fd-98ea-53a2e5692df7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnhancedStorageSiloAction, IEnhancedStorageSiloAction interface [Enhanced Storage], IEnhancedStorageSiloAction interface [Enhanced Storage],described, ehstorapi/IEnhancedStorageSiloAction, enstor.ienhancedstoragesiloaction
ms.topic: interface
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
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
 - EhStorAPI.h
api_name:
 - IEnhancedStorageSiloAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnhancedStorageSiloAction interface


## -description


 Use this interface as a point of access for actions involving IEEE 1667 silos.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnhancedStorageSiloAction</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnhancedStorageSiloAction</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnhancedStorageSiloAction</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1eb94182-520e-40a6-87e6-6ead2ab2e188">GetDescription</a>
</td>
<td align="left" width="63%">
Returns a descriptive string for the action specified by the <b>IEnhancedStorageSiloAction</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3690d395-c83e-4253-adc2-d30a96a5ce47">GetName</a>
</td>
<td align="left" width="63%">
Returns a string for the name of the action specified by the <b>IEnhancedStorageSiloAction</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f19cd0a-6d12-4e76-b46e-7c6267914223">Invoke</a>
</td>
<td align="left" width="63%">
Performs the action specified by an <b>IEnhancedStorageSiloAction</b> object.

</td>
</tr>
</table> 

