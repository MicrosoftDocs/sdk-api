---
UID: NF:gpmgmt.IGPMSitesContainer.SearchSites
title: IGPMSitesContainer::SearchSites (gpmgmt.h)
description: Retrieves a collection of scope of management (SOM) objects based on the specified search criteria. This method returns only site objects.
helpviewer_keywords: ["GPMSitesContainer class [GPMC]","SearchSites method","IGPMSitesContainer interface [GPMC]","SearchSites method","IGPMSitesContainer.SearchSites","IGPMSitesContainer::SearchSites","SearchSites","SearchSites method [GPMC]","SearchSites method [GPMC]","GPMSitesContainer class","SearchSites method [GPMC]","IGPMSitesContainer interface","_win32_igpmsitescontainer_searchsites","gpmc.igpmsitescontainer_searchsites","gpmgmt/IGPMSitesContainer::SearchSites","somLinks"]
old-location: gpmc\igpmsitescontainer_searchsites.htm
tech.root: gpmc
ms.assetid: bcbe1d94-ae82-4b33-8831-039896816a2d
ms.date: 12/05/2018
ms.keywords: GPMSitesContainer class [GPMC],SearchSites method, IGPMSitesContainer interface [GPMC],SearchSites method, IGPMSitesContainer.SearchSites, IGPMSitesContainer::SearchSites, SearchSites, SearchSites method [GPMC], SearchSites method [GPMC],GPMSitesContainer class, SearchSites method [GPMC],IGPMSitesContainer interface, _win32_igpmsitescontainer_searchsites, gpmc.igpmsitescontainer_searchsites, gpmgmt/IGPMSitesContainer::SearchSites, somLinks
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
 - IGPMSitesContainer::SearchSites
 - gpmgmt/IGPMSitesContainer::SearchSites
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
 - IGPMSitesContainer.SearchSites
 - GPMSitesContainer.SearchSites
---

## -description

Retrieves a collection of scope of management (SOM) objects based on the specified search criteria. This method returns only site objects.

## -parameters

### -param pIGPMSearchCriteria [in]

Pointer to criteria to supply to the search. Valid criteria for the search include the following.

#### somLinks

Pointer to an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> or an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface to query the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a> interface. For script programmers, this is a reference to a <b>GPMGPO</b> object.  Valid criteria includes the opContains search operator.

### -param ppIGPMSOMCollection [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsomcollection">IGPMSOMCollection</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSOMCollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSOMCollection</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsomcollection">IGPMSOMCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsitescontainer">IGPMSitesContainer</a>