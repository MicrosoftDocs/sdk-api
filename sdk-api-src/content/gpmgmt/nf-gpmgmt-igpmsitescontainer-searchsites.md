---
UID: NF:gpmgmt.IGPMSitesContainer.SearchSites
title: IGPMSitesContainer::SearchSites
author: windows-sdk-content
description: Retrieves a collection of scope of management (SOM) objects based on the specified search criteria. This method returns only site objects.
old-location: gpmc\igpmsitescontainer_searchsites.htm
tech.root: GPMC
ms.assetid: bcbe1d94-ae82-4b33-8831-039896816a2d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GPMSitesContainer class [GPMC],SearchSites method, IGPMSitesContainer interface [GPMC],SearchSites method, IGPMSitesContainer.SearchSites, IGPMSitesContainer::SearchSites, SearchSites, SearchSites method [GPMC], SearchSites method [GPMC],GPMSitesContainer class, SearchSites method [GPMC],IGPMSitesContainer interface, _win32_igpmsitescontainer_searchsites, gpmc.igpmsitescontainer_searchsites, gpmgmt/IGPMSitesContainer::SearchSites, somLinks
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IGPMSitesContainer.SearchSites
 - GPMSitesContainer.SearchSites
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gpmgmt.h
: 
- IGPMSitesContainer.SearchSites
: 
---

# IGPMSitesContainer::SearchSites


## -description


Retrieves a collection of scope of management (SOM) objects based on the specified search criteria. This method returns only site objects.


## -parameters




### -param pIGPMSearchCriteria [in]

Pointer to criteria to supply to the search. Valid criteria for the search include the following.



#### somLinks

Pointer to an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> or an <a href="_com_iunknown">IUnknown</a> interface to query the 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> interface. For script programmers, this is a reference to a <b>GPMGPO</b> object.  Valid criteria includes the opContains search operator.


### -param ppIGPMSOMCollection [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d">IGPMSOMCollection</a> interface.


#### - objGPMSearchCriteria


<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object to supply to the search.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSOMCollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSOMCollection</b> object.




## -see-also




<a href="https://msdn.microsoft.com/079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d">IGPMSOMCollection</a>



<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">IGPMSearchCriteria</a>



<a href="https://msdn.microsoft.com/e3fdfd44-9e90-4206-b7e9-97d4ed6eb8af">IGPMSitesContainer</a>
 

 

