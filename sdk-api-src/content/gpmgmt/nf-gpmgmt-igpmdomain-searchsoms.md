---
UID: NF:gpmgmt.IGPMDomain.SearchSOMs
title: IGPMDomain::SearchSOMs (gpmgmt.h)
description: Executes a search for GPMSOM objects (domains and organizational units) in the domain and then returns a GPMSOMCollection object.
helpviewer_keywords: ["GPMDomain object [GPMC]","SearchSOMs method","IGPMDomain interface [GPMC]","SearchSOMs method","IGPMDomain.SearchSOMs","IGPMDomain::SearchSOMs","SearchSOMs","SearchSOMs method [GPMC]","SearchSOMs method [GPMC]","GPMDomain object","SearchSOMs method [GPMC]","IGPMDomain interface","_win32_igpmdomain_searchsoms","gpmc.igpmdomain_searchsoms","gpmgmt/IGPMDomain::SearchSOMs","somLinks"]
old-location: gpmc\igpmdomain_searchsoms.htm
tech.root: gpmc
ms.assetid: 7ca3b0ef-b0d5-408a-8d75-647546087155
ms.date: 12/05/2018
ms.keywords: GPMDomain object [GPMC],SearchSOMs method, IGPMDomain interface [GPMC],SearchSOMs method, IGPMDomain.SearchSOMs, IGPMDomain::SearchSOMs, SearchSOMs, SearchSOMs method [GPMC], SearchSOMs method [GPMC],GPMDomain object, SearchSOMs method [GPMC],IGPMDomain interface, _win32_igpmdomain_searchsoms, gpmc.igpmdomain_searchsoms, gpmgmt/IGPMDomain::SearchSOMs, somLinks
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
 - IGPMDomain::SearchSOMs
 - gpmgmt/IGPMDomain::SearchSOMs
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
 - IGPMDomain.SearchSOMs
 - GPMDomain.SearchSOMs
---

## -description

Executes a search for 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">GPMSOM</a> objects (domains and organizational units) in the domain and then returns a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsomcollection">GPMSOMCollection</a> object.

## -parameters

### -param pIGPMSearchCriteria [in]

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> object to apply to the search.

### -param ppIGPMSOMCollection [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsomcollection">IGPMSOMCollection</a> interface that represents the scopes of management (SOMs) found by the search.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSOMCollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSOMCollection</b> object.

## -remarks

This method does not allow you to search for site SOMs. Call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsitescontainer-searchsites">IGPMSitesContainer::SearchSites</a> method to perform this type of search.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">IGPMSOM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsomcollection">IGPMSOMCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a>