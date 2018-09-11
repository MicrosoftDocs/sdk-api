---
UID: NF:gpmgmt.IGPMDomain.SearchWMIFilters
title: IGPMDomain::SearchWMIFilters
author: windows-sdk-content
description: Executes a search for GPMWMIFilter objects in the domain and then returns a GPMWMIFilterCollection object.
old-location: gpmc\igpmdomain_searchwmifilters.htm
tech.root: GPMC
ms.assetid: 4e0abc25-bdcb-4277-90bb-542e922fc71c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMDomain object [GPMC],SearchWMIFilters method, IGPMDomain interface [GPMC],SearchWMIFilters method, IGPMDomain.SearchWMIFilters, IGPMDomain::SearchWMIFilters, SearchWMIFilters, SearchWMIFilters method [GPMC], SearchWMIFilters method [GPMC],GPMDomain object, SearchWMIFilters method [GPMC],IGPMDomain interface, _win32_igpmdomain_searchwmifilters, gpmc.igpmdomain_searchwmifilters, gpmgmt/IGPMDomain::SearchWMIFilters
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
 - IGPMDomain.SearchWMIFilters
 - GPMDomain.SearchWMIFilters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMDomain::SearchWMIFilters


## -description


Executes a search for 
<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">GPMWMIFilter</a> objects in the domain and then returns a 
<a href="https://msdn.microsoft.com/8f65e6f6-fca3-46b7-aa0d-804470feb5bb">GPMWMIFilterCollection</a> object.


## -parameters




### -param pIGPMSearchCriteria [in]

This parameter should be <b>NULL</b>, or it should point to an empty <a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">IGPMSearchCriteria</a>  interface because no search criteria are allowed for WMI filters.


### -param ppIGPMWMIFilterCollection [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">IGPMWMIFilterCollection</a> interface that represents the WMI filters found by the search.


#### - objGPMSearchCriteria [in]


<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">GPMSearchCriteria</a> object to apply to the search. The <b>GPMSearchCriteria</b> object should be empty because no search criteria are allowed for Windows Management Instrumentation (WMI) filters.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/8f65e6f6-fca3-46b7-aa0d-804470feb5bb">GPMWMIFilterCollection</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/8f65e6f6-fca3-46b7-aa0d-804470feb5bb">GPMWMIFilterCollection</a> object.




## -remarks



An empty  <a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">GPMSearchCriteria</a> object is one that has had no criteria added to it. Passing in an empty <b>GPMSearchCriteria</b> object will return all WMI filters.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">IGPMSearchCriteria</a>



<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>



<a href="https://msdn.microsoft.com/8f65e6f6-fca3-46b7-aa0d-804470feb5bb">IGPMWMIFilterCollection</a>
 

 

