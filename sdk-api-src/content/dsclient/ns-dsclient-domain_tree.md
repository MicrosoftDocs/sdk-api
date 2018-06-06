---
UID: NS:dsclient.DOMAIN_TREE
title: DOMAIN_TREE
author: windows-sdk-content
description: The DOMAINTREE structure contains data about a node in a domain tree obtained with the IDsBrowseDomainTree::GetDomains method. Each of the domains in the tree node are represented by a DOMAINDESC structure.
old-location: ad\domaintree.htm
old-project: AD
ms.assetid: c4b3f81c-0632-407c-834e-8eec6fefde68
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDOMAINTREE, *PDOMAIN_TREE, DOMAINTREE, DOMAINTREE structure [Active Directory], DOMAIN_TREE, DOMAIN_TREE structure [Active Directory], LPDOMAINTREE, LPDOMAINTREE structure pointer [Active Directory], PDOMAIN_TREE, PDOMAIN_TREE structure pointer [Active Directory], _glines_domaintree, ad.domaintree, dsclient/DOMAINTREE, dsclient/DOMAIN_TREE, dsclient/LPDOMAINTREE, dsclient/PDOMAIN_TREE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DOMAIN_TREE, DOMAINTREE, *PDOMAIN_TREE, *LPDOMAINTREE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsclient.h
api_name:
 - DOMAINTREE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DOMAIN_TREE structure


## -description


The <b>DOMAINTREE</b> structure contains  data about a node in a domain tree obtained with the <a href="https://msdn.microsoft.com/42cd38c2-7470-49b5-9b64-d971f2a915c6">IDsBrowseDomainTree::GetDomains</a> method. Each of the domains in the tree  node are represented by a 
<a href="https://msdn.microsoft.com/c788d106-2cc7-4d67-8568-23e858c0075f">DOMAINDESC</a> structure.


## -struct-fields




### -field dsSize

Contains the size, in bytes, of the <b>DOMAINTREE</b> structure and all <a href="https://msdn.microsoft.com/c788d106-2cc7-4d67-8568-23e858c0075f">DOMAINDESC</a> structures in this <b>DOMAINTREE</b> structure.


### -field dwCount

Contains the number of  <a href="https://msdn.microsoft.com/c788d106-2cc7-4d67-8568-23e858c0075f">DOMAINDESC</a> structures in the <b>aDomains</b> array.


### -field aDomains

Contains an array of <a href="https://msdn.microsoft.com/c788d106-2cc7-4d67-8568-23e858c0075f">DOMAINDESC</a> structures that represent the domains. The array does not contain any child or sibling relational data. The relational data is contained within the <b>DOMAINDESC</b> structures.


## -remarks



For more information about how to access and use the data in this structure, see <a href="https://msdn.microsoft.com/26793c61-469e-4e99-9056-b9fc04336b69">Domain Browser</a>.




## -see-also




<a href="https://msdn.microsoft.com/c788d106-2cc7-4d67-8568-23e858c0075f">DOMAINDESC</a>



<a href="https://msdn.microsoft.com/26793c61-469e-4e99-9056-b9fc04336b69">Domain Browser</a>



<a href="https://msdn.microsoft.com/d9334f4c-d5b0-445a-ad1b-8628f206b715">IDsBrowseDomainTree::FreeDomains</a>



<a href="https://msdn.microsoft.com/42cd38c2-7470-49b5-9b64-d971f2a915c6">IDsBrowseDomainTree::GetDomains</a>
 

 

