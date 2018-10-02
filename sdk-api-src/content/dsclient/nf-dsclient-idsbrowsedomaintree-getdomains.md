---
UID: NF:dsclient.IDsBrowseDomainTree.GetDomains
title: IDsBrowseDomainTree::GetDomains
author: windows-sdk-content
description: The IDsBrowseDomainTree::GetDomains method retrieves the trust domains of the current computer. The current computer is set using the IDsBrowseDomainTree::SetComputer method.
old-location: ad\idsbrowsedomaintree_getdomains.htm
tech.root: AD
ms.assetid: 42cd38c2-7470-49b5-9b64-d971f2a915c6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DBDTF_RETURNEXTERNAL, DBDTF_RETURNFQDN, DBDTF_RETURNINBOUND, DBDTF_RETURNINOUTBOUND, DBDTF_RETURNMIXEDDOMAINS, GetDomains, GetDomains method [Active Directory], GetDomains method [Active Directory],IDsBrowseDomainTree interface, IDsBrowseDomainTree interface [Active Directory],GetDomains method, IDsBrowseDomainTree.GetDomains, IDsBrowseDomainTree::GetDomains, _glines_idsbrowsedomaintree_getdomains, ad.idsbrowsedomaintree__getdomains, ad.idsbrowsedomaintree_getdomains, dsclient/IDsBrowseDomainTree::GetDomains
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
 - IDsBrowseDomainTree.GetDomains
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsBrowseDomainTree::GetDomains


## -description


The <b>IDsBrowseDomainTree::GetDomains</b> method retrieves the trust domains of the current computer.
  The current computer is set using the <a href="https://msdn.microsoft.com/1e070673-ce8d-4f68-a066-5baf38180745">IDsBrowseDomainTree::SetComputer</a> method.


## -parameters




### -param ppDomainTree [in]

Pointer to a <a href="https://msdn.microsoft.com/c4b3f81c-0632-407c-834e-8eec6fefde68">DOMAINTREE</a> structure pointer that receives the trust domain data. The caller must free this memory when no longer required by calling <a href="https://msdn.microsoft.com/d9334f4c-d5b0-445a-ad1b-8628f206b715">IDsBrowseDomainTree::FreeDomains</a>.


### -param dwFlags [in]

Contains a set of flags that modify the domain contents. This can be zero or a combination of one or more of the following values.



#### DBDTF_RETURNFQDN

The <b>pszNCName</b> members of the <a href="https://msdn.microsoft.com/c788d106-2cc7-4d67-8568-23e858c0075f">DOMAINDESC</a> structures will receive the fully qualified domain names. The fully qualified domain name takes the form "DC=myDom, DC=Fabrikam, DC=com" as opposed to "myDom.Fabrikam.com".



#### DBDTF_RETURNMIXEDDOMAINS

The method will return downlevel trust domains.



#### DBDTF_RETURNEXTERNAL

The method will return external trust domains.



#### DBDTF_RETURNINBOUND

If this flag is set, the method returns trusting domains. If this flag is not set, the method returns trusted domains.



#### DBDTF_RETURNINOUTBOUND

The method will return both trusted and trusting domains.


## -returns



Returns a standard <b>HRESULT</b> value including the following.




## -remarks



For more information about how to access and use the data provided by this method, see <a href="https://msdn.microsoft.com/26793c61-469e-4e99-9056-b9fc04336b69">Domain Browser</a>.




## -see-also




<a href="https://msdn.microsoft.com/c788d106-2cc7-4d67-8568-23e858c0075f">DOMAINDESC</a>



<a href="https://msdn.microsoft.com/c4b3f81c-0632-407c-834e-8eec6fefde68">DOMAINTREE</a>



<a href="https://msdn.microsoft.com/26793c61-469e-4e99-9056-b9fc04336b69">Domain Browser</a>



<a href="https://msdn.microsoft.com/f50caa34-d29e-4ad1-98b0-ef5c1f5550bf">IDsBrowseDomainTree</a>



<a href="https://msdn.microsoft.com/d9334f4c-d5b0-445a-ad1b-8628f206b715">IDsBrowseDomainTree::FreeDomains</a>
 

 

