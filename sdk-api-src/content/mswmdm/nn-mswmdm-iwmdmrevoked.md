---
UID: NN:mswmdm.IWMDMRevoked
title: IWMDMRevoked (mswmdm.h)
author: windows-sdk-content
description: The IWMDMRevoked interface retrieves the URL from which updated components can be downloaded, if a transfer fails with a revocation error.
old-location: wmdm\iwmdmrevoked.htm
tech.root: WMDM
ms.assetid: b627f243-3652-4db9-8a5e-6a2146b73424
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMDMRevoked, IWMDMRevoked interface [windows Media Device Manager], IWMDMRevoked interface [windows Media Device Manager],described, IWMDMRevokedInterface, mswmdm/IWMDMRevoked, wmdm.iwmdmrevoked
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
 - IWMDMRevoked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMRevoked interface


## -description



The <b>IWMDMRevoked</b> interface retrieves the URL from which updated components can be downloaded, if a transfer fails with a revocation error. The secured content provider determines whether or not to allow a transfer, based on the application certificates of the components involved. You can access the <b>IWMDMRevoked</b> interface by calling <b>QueryInterface</b> on the <a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMRevoked</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMRevoked</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMRevoked</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0158a664-8f0b-4481-8028-46b05776a482">GetRevocationURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL from which updated components can be downloaded.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

