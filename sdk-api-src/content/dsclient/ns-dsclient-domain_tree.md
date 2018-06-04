---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

