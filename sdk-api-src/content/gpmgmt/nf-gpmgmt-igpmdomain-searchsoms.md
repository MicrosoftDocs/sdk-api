---
UID: NF:gpmgmt.IGPMDomain.SearchSOMs
title: IGPMDomain::SearchSOMs (gpmgmt.h)
author: windows-sdk-content
description: Executes a search for GPMSOM objects (domains and organizational units) in the domain and then returns a GPMSOMCollection object.
old-location: gpmc\igpmdomain_searchsoms.htm
tech.root: gpmc
ms.assetid: 7ca3b0ef-b0d5-408a-8d75-647546087155
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMDomain object [GPMC],SearchSOMs method, IGPMDomain interface [GPMC],SearchSOMs method, IGPMDomain.SearchSOMs, IGPMDomain::SearchSOMs, SearchSOMs, SearchSOMs method [GPMC], SearchSOMs method [GPMC],GPMDomain object, SearchSOMs method [GPMC],IGPMDomain interface, _win32_igpmdomain_searchsoms, gpmc.igpmdomain_searchsoms, gpmgmt/IGPMDomain::SearchSOMs, somLinks
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMDomain.SearchSOMs
 - GPMDomain.SearchSOMs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMDomain::SearchSOMs


## -description


Executes a search for 
<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">GPMSOM</a> objects (domains and organizational units) in the domain and then returns a 
<a href="https://msdn.microsoft.com/079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d">GPMSOMCollection</a> object.


## -parameters




### -param pIGPMSearchCriteria [in]

Criteria to apply to the search. The valid criteria for the search include the following values.



#### somLinks

Pointer to an <b>IDispatch</b> or <b>IUnknown</b> interface to query the 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> interface. For script programmers, this is a reference to a <b>GPMGPO</b> object.   The valid criteria include the <b>opContains</b> search operator.


### -param ppIGPMSOMCollection [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d">IGPMSOMCollection</a> interface that represents the scopes of management (SOMs) found by the search.


#### - objGPMSearchCriteria


<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">GPMSearchCriteria</a> object to apply to the search.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSOMCollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSOMCollection</b> object.




## -remarks



This method does not allow you to search for site SOMs. Call the 
<a href="https://msdn.microsoft.com/bcbe1d94-ae82-4b33-8831-039896816a2d">IGPMSitesContainer::SearchSites</a> method to perform this type of search.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">IGPMSOM</a>



<a href="https://msdn.microsoft.com/079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d">IGPMSOMCollection</a>



<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">IGPMSearchCriteria</a>
 

 

