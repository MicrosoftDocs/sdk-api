---
UID: NF:gpmgmt.IGPMDomain.SearchWMIFilters
title: IGPMDomain::SearchWMIFilters (gpmgmt.h)
author: windows-sdk-content
description: Executes a search for GPMWMIFilter objects in the domain and then returns a GPMWMIFilterCollection object.
old-location: gpmc\igpmdomain_searchwmifilters.htm
tech.root: gpmc
ms.assetid: 4e0abc25-bdcb-4277-90bb-542e922fc71c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMDomain object [GPMC],SearchWMIFilters method, IGPMDomain interface [GPMC],SearchWMIFilters method, IGPMDomain.SearchWMIFilters, IGPMDomain::SearchWMIFilters, SearchWMIFilters, SearchWMIFilters method [GPMC], SearchWMIFilters method [GPMC],GPMDomain object, SearchWMIFilters method [GPMC],IGPMDomain interface, _win32_igpmdomain_searchwmifilters, gpmc.igpmdomain_searchwmifilters, gpmgmt/IGPMDomain::SearchWMIFilters
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
ms.custom: 19H1
---

# IGPMDomain::SearchWMIFilters


## -description


Executes a search for 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> objects in the domain and then returns a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">GPMWMIFilterCollection</a> object.


## -parameters




### -param pIGPMSearchCriteria [in]

This parameter should be <b>NULL</b>, or it should point to an empty <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a>  interface because no search criteria are allowed for WMI filters.


### -param ppIGPMWMIFilterCollection [out]

Address of a pointer to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMWMIFilterCollection</a> interface that represents the WMI filters found by the search.


#### - objGPMSearchCriteria [in]


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> object to apply to the search. The <b>GPMSearchCriteria</b> object should be empty because no search criteria are allowed for Windows Management Instrumentation (WMI) filters.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">GPMWMIFilterCollection</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">GPMWMIFilterCollection</a> object.




## -remarks



An empty  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> object is one that has had no criteria added to it. Passing in an empty <b>GPMSearchCriteria</b> object will return all WMI filters.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">IGPMWMIFilterCollection</a>
 

 

