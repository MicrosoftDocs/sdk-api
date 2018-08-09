---
UID: NS:dsclient._DOMAINDESC
title: "_DOMAINDESC"
author: windows-sdk-content
description: Contains data about an element in a domain tree obtained with the IDsBrowseDomainTree::GetDomains method.
old-location: ad\domaindesc.htm
old-project: ad
ms.assetid: c788d106-2cc7-4d67-8568-23e858c0075f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDOMAINDESC, *PDOMAIN_DESC, DOMAINDESC, DOMAINDESC structure [Active Directory], DOMAIN_DESC, DOMAIN_DESC structure [Active Directory], LPDOMAINDESC, LPDOMAINDESC structure pointer [Active Directory], PDOMAIN_DESC, PDOMAIN_DESC structure pointer [Active Directory], _DOMAINDESC, _glines_domaindesc, ad.domaindesc, dsclient/DOMAINDESC, dsclient/LPDOMAINDESC, dsclient/PDOMAIN_DESC"
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
req.typenames: DOMAIN_DESC, DOMAINDESC, *PDOMAIN_DESC, *LPDOMAINDESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsclient.h
api_name:
 - DOMAIN_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

