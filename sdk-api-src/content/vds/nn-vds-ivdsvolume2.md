---
UID: NN:vds.IVdsVolume2
title: IVdsVolume2
author: windows-sdk-content
description: Provides a method for returning volume property information, including the volume GUIDs.
old-location: base\ivdsvolume2.htm
tech.root: vds
ms.assetid: 78077ce6-04f7-4d76-9057-40941feb941b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsVolume2, IVdsVolume2 interface, IVdsVolume2 interface,described, base.ivdsvolume2, vds/IVdsVolume2
ms.topic: interface
req.header: vds.h
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVolume2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVolume2 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method for returning volume property information, including the volume GUIDs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolume2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsVolume2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolume2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9580ceb2-6b2f-4313-a140-f6fa6a366960">GetProperties2</a>
</td>
<td align="left" width="63%">
Returns 
   property information for the current volume. This method is identical to the <a href="https://msdn.microsoft.com/ba4a92c9-35f1-463a-8fa3-1a0d78720555">IVdsVolume::GetProperties</a> method, except that it returns a <a href="https://msdn.microsoft.com/e99aaead-f5ad-4181-9208-9158e9fac38f">VDS_VOLUME_PROP2</a> structure instead of a <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a> structure.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a02ee0a6-ac29-406c-9fc0-4f632d32424f">IVdsVolume</a>
 

 

