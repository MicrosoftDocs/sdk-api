---
UID: NN:dsclient.IDsBrowseDomainTree
title: IDsBrowseDomainTree
author: windows-sdk-content
description: The IDsBrowseDomainTree interface is used by an application to display a domain browser dialog box and/or obtain a list of trust domains related to a given computer.
old-location: ad\idsbrowsedomaintree.htm
tech.root: ad
ms.assetid: f50caa34-d29e-4ad1-98b0-ef5c1f5550bf
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IDsBrowseDomainTree, IDsBrowseDomainTree interface [Active Directory], IDsBrowseDomainTree interface [Active Directory],described, _glines_idsbrowsedomaintree, ad.idsbrowsedomaintree, dsclient/IDsBrowseDomainTree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dsclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Dsadmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsBrowseDomainTree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsBrowseDomainTree interface


## -description


The <b>IDsBrowseDomainTree</b> interface is used by an application to display a domain browser dialog box and/or obtain a list of trust domains related to a given computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsBrowseDomainTree</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDsBrowseDomainTree</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDsBrowseDomainTree</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22b719fc-bd46-44c6-a690-af6e9767f9ce">BrowseTo</a>
</td>
<td align="left" width="63%">
Displays a dialog box used to browse for a domain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6f4dbbb-5e2f-470a-bfc0-5bb6e96c7a6c">FlushCachedDomains</a>
</td>
<td align="left" width="63%">
Frees the cached domain list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9334f4c-d5b0-445a-ad1b-8628f206b715">FreeDomains</a>
</td>
<td align="left" width="63%">
Frees the memory allocated by the <a href="https://msdn.microsoft.com/42cd38c2-7470-49b5-9b64-d971f2a915c6">IDsBrowseDomainTree::GetDomains</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42cd38c2-7470-49b5-9b64-d971f2a915c6">GetDomains</a>
</td>
<td align="left" width="63%">
Retrieves the trust domains of the current computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e070673-ce8d-4f68-a066-5baf38180745">SetComputer</a>
</td>
<td align="left" width="63%">
Specifies the computer and credentials to be used by this instance of the <b>IDsBrowseDomainTree</b> interface.

</td>
</tr>
</table> 


## -remarks



An instance of this interface is created by calling <a href="_com_cocreateinstance">CoCreateInstance</a> with the <b>CLSID_DsDomainTreeBrowser</b> class identifier as shown below.


```cpp
HRESULT hr = S_OK;
IDsBrowseDomainTree *pDSB = NULL;

hr = CoCreateInstance(    CLSID_DsDomainTreeBrowser,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDsBrowseDomainTree,
                          (void**)&pDSB);

if(SUCCEEDED(hr))
{
    //use the IDsBrowseDomainTree object

    //release the IDsBrowseDomainTree object
    pDSB->Release();
}
```





## -see-also




<a href="_com_cocreateinstance">CoCreateInstance</a>
 

 

