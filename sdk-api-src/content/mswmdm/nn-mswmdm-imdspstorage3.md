---
UID: NN:mswmdm.IMDSPStorage3
title: IMDSPStorage3 (mswmdm.h)
author: windows-sdk-content
description: The IMDSPStorage3 interface extends IMDSPStorage2 by supporting metadata.
old-location: wmdm\imdspstorage3.htm
tech.root: WMDM
ms.assetid: 5ff674a1-a0b9-43b6-b8b7-9a5c67b3f919
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPStorage3, IMDSPStorage3 interface [windows Media Device Manager], IMDSPStorage3 interface [windows Media Device Manager],described, IMDSPStorage3Interface, mswmdm/IMDSPStorage3, wmdm.imdspstorage3
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IMDSPStorage3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPStorage3 interface


## -description



The <b>IMDSPStorage3</b> interface extends <a href="https://msdn.microsoft.com/39afb282-7141-4eb5-93e9-a69bef495d80">IMDSPStorage2</a> by supporting metadata. This interface is optional. Service providers must implement this interface only if they are going to support metadata. If the device parameter <i>UseMetadataViews</i> is set to 1, this interface must be implemented and the <b>GetMetadata</b> method becomes mandatory, although <b>SetMetadata</b> is still optional. For more information, see <a href="https://msdn.microsoft.com/d8774c85-b5c0-4d9e-8a8e-d60ffdf59549">Device Parameters</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPStorage3</b> interface inherits from <a href="https://msdn.microsoft.com/39afb282-7141-4eb5-93e9-a69bef495d80">IMDSPStorage2</a>. <b>IMDSPStorage3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPStorage3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a341289b-79e6-4ac7-b0d3-72ad5953c1df">GetMetadata</a>
</td>
<td align="left" width="63%">
Retrieves metadata from the service provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfb9a1e4-3cf6-4605-9613-d93f9cce201b">SetMetadata</a>
</td>
<td align="left" width="63%">
Provides the metadata associated with a specified content.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/39afb282-7141-4eb5-93e9-a69bef495d80">IMDSPStorage2 Interface</a>



<a href="https://msdn.microsoft.com/c1236acc-1f11-4501-9374-2486f7d61db3">IMDSPStorage4 Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

