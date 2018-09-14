---
UID: NF:dsclient.IDsBrowseDomainTree.SetComputer
title: IDsBrowseDomainTree::SetComputer
author: windows-sdk-content
description: Specifies the computer and credentials to be used by this instance of the IDsBrowseDomainTree interface.
old-location: ad\idsbrowsedomaintree_setcomputer.htm
tech.root: ad
ms.assetid: 1e070673-ce8d-4f68-a066-5baf38180745
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: IDsBrowseDomainTree interface [Active Directory],SetComputer method, IDsBrowseDomainTree.SetComputer, IDsBrowseDomainTree::SetComputer, SetComputer, SetComputer method [Active Directory], SetComputer method [Active Directory],IDsBrowseDomainTree interface, _glines_idsbrowsedomaintree_setcomputer, ad.idsbrowsedomaintree__setcomputer, ad.idsbrowsedomaintree_setcomputer, dsclient/IDsBrowseDomainTree::SetComputer
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
 - IDsBrowseDomainTree.SetComputer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsBrowseDomainTree::SetComputer


## -description


The <b>IDsBrowseDomainTree::SetComputer</b> method specifies the computer and credentials to be used by this instance of the <a href="https://msdn.microsoft.com/f50caa34-d29e-4ad1-98b0-ef5c1f5550bf">IDsBrowseDomainTree</a> interface.


## -parameters




### -param pszComputerName [in]

Pointer to a null-terminated Unicode string that contains the name of the target computer.


### -param pszUserName [in]

Pointer to a null-terminated Unicode string that contains the user name used to access the  computer.


### -param pszPassword [in]

Pointer to a null-terminated Unicode string that contains the password used to access the  computer.


## -returns



Returns a standard <b>HRESULT</b> value including the following.




## -remarks



If this method is not called, the local host is assumed as the default computer.

When <b>SetComputer</b> is called on a particular <a href="https://msdn.microsoft.com/f50caa34-d29e-4ad1-98b0-ef5c1f5550bf">IDsBrowseDomainTree</a> instance, <a href="https://msdn.microsoft.com/e6f4dbbb-5e2f-470a-bfc0-5bb6e96c7a6c">IDsBrowseDomainTree::FlushCachedDomains</a> must be called before <b>SetComputer</b> is called again.




## -see-also




<a href="https://msdn.microsoft.com/f50caa34-d29e-4ad1-98b0-ef5c1f5550bf">IDsBrowseDomainTree</a>



<a href="https://msdn.microsoft.com/e6f4dbbb-5e2f-470a-bfc0-5bb6e96c7a6c">IDsBrowseDomainTree::FlushCachedDomains</a>
 

 

