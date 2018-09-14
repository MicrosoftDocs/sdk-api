---
UID: NF:dsclient.IDsBrowseDomainTree.FreeDomains
title: IDsBrowseDomainTree::FreeDomains
author: windows-sdk-content
description: The IDsBrowseDomainTree::FreeDomains method frees the memory allocated by the IDsBrowseDomainTree::GetDomains method.
old-location: ad\idsbrowsedomaintree_freedomains.htm
tech.root: ad
ms.assetid: d9334f4c-d5b0-445a-ad1b-8628f206b715
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: FreeDomains, FreeDomains method [Active Directory], FreeDomains method [Active Directory],IDsBrowseDomainTree interface, IDsBrowseDomainTree interface [Active Directory],FreeDomains method, IDsBrowseDomainTree.FreeDomains, IDsBrowseDomainTree::FreeDomains, _glines_idsbrowsedomaintree_freedomains, ad.idsbrowsedomaintree__freedomains, ad.idsbrowsedomaintree_freedomains, dsclient/IDsBrowseDomainTree::FreeDomains
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDsBrowseDomainTree.FreeDomains
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsBrowseDomainTree::FreeDomains


## -description


The <b>IDsBrowseDomainTree::FreeDomains</b> method frees the memory allocated by the <a href="https://msdn.microsoft.com/42cd38c2-7470-49b5-9b64-d971f2a915c6">IDsBrowseDomainTree::GetDomains</a> method.


## -parameters




### -param ppDomainTree [in]

Pointer to the 
<a href="https://msdn.microsoft.com/c4b3f81c-0632-407c-834e-8eec6fefde68">DOMAINTREE</a> data structure.


## -returns



Returns a standard <b>HRESULT</b> value including the following.




## -see-also




<a href="https://msdn.microsoft.com/f50caa34-d29e-4ad1-98b0-ef5c1f5550bf">IDsBrowseDomainTree</a>



<a href="https://msdn.microsoft.com/42cd38c2-7470-49b5-9b64-d971f2a915c6">IDsBrowseDomainTree::GetDomains</a>
 

 

