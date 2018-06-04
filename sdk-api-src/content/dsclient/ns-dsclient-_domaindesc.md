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

# _DOMAINDESC structure


## -description


The <b>DOMAINDESC</b> structure contains data about an element in a domain tree obtained with the <a href="https://msdn.microsoft.com/42cd38c2-7470-49b5-9b64-d971f2a915c6">IDsBrowseDomainTree::GetDomains</a> method. This structure is contained in the <a href="https://msdn.microsoft.com/c4b3f81c-0632-407c-834e-8eec6fefde68">DOMAINTREE</a> structure.


## -struct-fields




### -field pszName

Pointer to a Unicode string that contains the domain name.


### -field pszPath

Pointer to a Unicode string that contains the path of the domain. Reserved.


### -field pszNCName

Pointer to a Unicode string that contains the fully qualified name of the domain in the form "DC=myDom, DC=Fabrikam, DC=com". This member is  blank if the <b>DBDTF_RETURNFQDN</b> flag is not set in the <i>dwFlags</i> parameter in <a href="https://msdn.microsoft.com/42cd38c2-7470-49b5-9b64-d971f2a915c6">IDsBrowseDomainTree::GetDomains</a>.


### -field pszTrustParent

Pointer to a Unicode string that contains the name of the parent domain. This member is <b>NULL</b> if the domain has no parent.


### -field pszObjectClass

Pointer to a Unicode string that contains the object class name of the domain.


### -field ulFlags

Contains a set of flags that specify the attributes of the trust. For more information, and a list of possible values, see the <i>Flags</i> parameter of <a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a>.


### -field fDownLevel

Contains a nonzero value if the domain is a down-level domain or zero otherwise.


### -field pdChildList

Contains a pointer to a <b>DOMAINDESC</b> structure that represents the first child of the domain. Obtain subsequent children by accessing the <b>pdNextSibling</b> member of the child structure. This member is <b>NULL</b> if the domain has no children.


### -field pdNextSibling

Contains a pointer to a <b>DOMAINDESC</b> structure that represents the next sibling of the domain. Obtain subsequent siblings by accessing the <b>pdNextSibling</b> member of the sibling structure. This member is <b>NULL</b> if the domain has no siblings.


## -remarks



For more information about how to access and use the information in this structure, see <a href="https://msdn.microsoft.com/26793c61-469e-4e99-9056-b9fc04336b69">Domain Browser</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4b3f81c-0632-407c-834e-8eec6fefde68">DOMAINTREE</a>



<a href="https://msdn.microsoft.com/bf6aa066-ee7e-4b13-9a4b-1e097632ec5a">Display Structures in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/26793c61-469e-4e99-9056-b9fc04336b69">Domain Browser</a>



<a href="https://msdn.microsoft.com/6c3b788f-ee53-4637-acdb-04316e8464fe">DsEnumerateDomainTrusts</a>
 

 

