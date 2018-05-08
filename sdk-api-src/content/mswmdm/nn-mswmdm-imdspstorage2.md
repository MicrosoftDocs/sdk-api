---
UID: NN:mswmdm.IMDSPStorage2
title: IMDSPStorage2
author: windows-driver-content
description: The IMDSPStorage2 interface extends IMDSPStorage by providing methods for getting and setting extended attributes and making it possible to get a pointer to a storage medium from its name.
old-location: wmdm\imdspstorage2.htm
old-project: WMDM
ms.assetid: 39afb282-7141-4eb5-93e9-a69bef495d80
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IMDSPStorage2, IMDSPStorage2 interface [windows Media Device Manager], IMDSPStorage2 interface [windows Media Device Manager],described, IMDSPStorage2Interface, mswmdm/IMDSPStorage2, wmdm.imdspstorage2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	IMDSPStorage2
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMDSPStorage2 interface


## -description



The <b>IMDSPStorage2</b> interface extends <a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage</a> by providing methods for getting and setting extended attributes and making it possible to get a pointer to a storage medium from its name. This interface also extends the <b>CreateStorage</b> method of the <b>IMDSPStorage</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPStorage2</b> interface inherits from <a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage</a>. <b>IMDSPStorage2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPStorage2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f79f4bf5-948e-4201-a9bc-edde4dd333ea">CreateStorage2</a>
</td>
<td align="left" width="63%">
Creates storage for a file to be copied to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2db30715-cd49-4e55-b0d0-73ac531f8661">GetAttributes2</a>
</td>
<td align="left" width="63%">
Gets attributes of files or storages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ddfdfc8-db43-4acc-aebc-617d3e746a4f">GetStorage</a>
</td>
<td align="left" width="63%">
Gets a storage pointer and a string containing the name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9c3f7e4-88b1-4842-aaaa-e6c52e1c3116">SetAttributes2</a>
</td>
<td align="left" width="63%">
Sets storage attributes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/5ff674a1-a0b9-43b6-b8b7-9a5c67b3f919">IMDSPStorage3 Interface</a>



<a href="https://msdn.microsoft.com/c1236acc-1f11-4501-9374-2486f7d61db3">IMDSPStorage4 Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

