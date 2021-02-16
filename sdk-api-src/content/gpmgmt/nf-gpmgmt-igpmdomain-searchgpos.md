---
UID: NF:gpmgmt.IGPMDomain.SearchGPOs
title: IGPMDomain::SearchGPOs (gpmgmt.h)
description: Executes a search for GPMGPO objects in the domain and then returns a GPMGPOCollection object.
helpviewer_keywords: ["GPMDomain object [GPMC]","SearchGPOs method","IGPMDomain interface [GPMC]","SearchGPOs method","IGPMDomain.SearchGPOs","IGPMDomain::SearchGPOs","SearchGPOs","SearchGPOs method [GPMC]","SearchGPOs method [GPMC]","GPMDomain object","SearchGPOs method [GPMC]","IGPMDomain interface","_win32_igpmdomain_searchgpos","gpmc.igpmdomain_searchgpos","gpmgmt/IGPMDomain::SearchGPOs","gpoComputerExtensions","gpoDisplayName","gpoEffectivePermissions","gpoID","gpoPermissions","gpoUserExtensions","gpoWMIFilter"]
old-location: gpmc\igpmdomain_searchgpos.htm
tech.root: gpmc
ms.assetid: 19a8efae-0b85-49ba-bf7e-08ed700874c3
ms.date: 12/05/2018
ms.keywords: GPMDomain object [GPMC],SearchGPOs method, IGPMDomain interface [GPMC],SearchGPOs method, IGPMDomain.SearchGPOs, IGPMDomain::SearchGPOs, SearchGPOs, SearchGPOs method [GPMC], SearchGPOs method [GPMC],GPMDomain object, SearchGPOs method [GPMC],IGPMDomain interface, _win32_igpmdomain_searchgpos, gpmc.igpmdomain_searchgpos, gpmgmt/IGPMDomain::SearchGPOs, gpoComputerExtensions, gpoDisplayName, gpoEffectivePermissions, gpoID, gpoPermissions, gpoUserExtensions, gpoWMIFilter
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
 - IGPMDomain::SearchGPOs
 - gpmgmt/IGPMDomain::SearchGPOs
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
 - IGPMDomain.SearchGPOs
 - GPMDomain.SearchGPOs
---

## -description

Executes a search for 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> objects in the domain and then returns a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">GPMGPOCollection</a> object.

## -parameters

### -param pIGPMSearchCriteria [in]

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> object to apply to the search.
Pointer to the criteria to apply to the search.

### -param ppIGPMGPOCollection [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMGPOCollection</a> interface representing the GPOs found by the search.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">GPMGPOCollection</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">GPMGPOCollection</a> object.

## -remarks

An empty  <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> object is one that has had no criteria added to it. Passing in an empty <b>GPMSearchCriteria</b> object will return all GPOs in the domain.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMGPOCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a>