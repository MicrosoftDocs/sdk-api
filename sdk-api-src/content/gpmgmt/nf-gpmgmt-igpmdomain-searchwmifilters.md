---
UID: NF:gpmgmt.IGPMDomain.SearchWMIFilters
title: IGPMDomain::SearchWMIFilters (gpmgmt.h)
description: Executes a search for GPMWMIFilter objects in the domain and then returns a GPMWMIFilterCollection object.
helpviewer_keywords: ["GPMDomain object [GPMC]","SearchWMIFilters method","IGPMDomain interface [GPMC]","SearchWMIFilters method","IGPMDomain.SearchWMIFilters","IGPMDomain::SearchWMIFilters","SearchWMIFilters","SearchWMIFilters method [GPMC]","SearchWMIFilters method [GPMC]","GPMDomain object","SearchWMIFilters method [GPMC]","IGPMDomain interface","_win32_igpmdomain_searchwmifilters","gpmc.igpmdomain_searchwmifilters","gpmgmt/IGPMDomain::SearchWMIFilters"]
old-location: gpmc\igpmdomain_searchwmifilters.htm
tech.root: gpmc
ms.assetid: 4e0abc25-bdcb-4277-90bb-542e922fc71c
ms.date: 12/05/2018
ms.keywords: GPMDomain object [GPMC],SearchWMIFilters method, IGPMDomain interface [GPMC],SearchWMIFilters method, IGPMDomain.SearchWMIFilters, IGPMDomain::SearchWMIFilters, SearchWMIFilters, SearchWMIFilters method [GPMC], SearchWMIFilters method [GPMC],GPMDomain object, SearchWMIFilters method [GPMC],IGPMDomain interface, _win32_igpmdomain_searchwmifilters, gpmc.igpmdomain_searchwmifilters, gpmgmt/IGPMDomain::SearchWMIFilters
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMDomain::SearchWMIFilters
 - gpmgmt/IGPMDomain::SearchWMIFilters
dev_langs:
 - c++
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
---

## -description

Executes a search for 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> objects in the domain and then returns a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">GPMWMIFilterCollection</a> object.

## -parameters

### -param pIGPMSearchCriteria [in]

This parameter should be <b>NULL</b>, or it should point to an empty <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a> interface, because no search criteria are allowed for Windows Management Instrumentation (WMI) filters.

### -param ppIGPMWMIFilterCollection [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMWMIFilterCollection</a> interface that represents the WMI filters found by the search.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">GPMWMIFilterCollection</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">GPMWMIFilterCollection</a> object.

## -remarks

An empty  <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> object is one that has had no criteria added to it. Passing in an empty <b>GPMSearchCriteria</b> object will return all WMI filters.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">IGPMWMIFilterCollection</a>