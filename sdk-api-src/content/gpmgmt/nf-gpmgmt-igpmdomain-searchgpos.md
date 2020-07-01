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
f1_keywords:
- gpmgmt/IGPMDomain.SearchGPOs
dev_langs:
- c++
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
- IGPMDomain.SearchGPOs
- GPMDomain.SearchGPOs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMDomain::SearchGPOs


## -description


Executes a search for 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> objects in the domain and then returns a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">GPMGPOCollection</a> object.


## -parameters




### -param pIGPMSearchCriteria [in]

Pointer to the criteria to apply to the search.



#### gpoDisplayName

Pointer to a  friendly Group Policy object (GPO) display name search. The search property value is the friendly GPO display name. Valid criteria include the <b>opEquals</b>, 
<b>opContains</b>, and <b>opNotContains</b> search operators.



#### gpoPermissions

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> or <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface to query the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a> interface. For script programmers, this is a reference to a <b>GPMPermission</b> object. Valid criteria include the <b>opContains</b> and <b>opNotContains</b> search operators.



#### gpoEffectivePermissions

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> or an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface to query the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a> interface. Valid criteria includes opContains or opNotContains search operator.



#### gpoWMIFilter

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> or an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface to query the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a> interface. Valid criteria includes opEquals or opNotEquals search operator.



#### gpoID

Pointer to a string containing a GUID that represents the group policy object's ID. Valid criteria includes opEquals or opNotEquals search operator.



#### gpoComputerExtensions

Pointer to a string containing a GUID that represents the client-side extension's ID. Valid criteria includes opContains or opNotContains search operator.



#### gpoUserExtensions

Pointer to a string containing a GUID that represents the user extension's ID.
 Valid criteria includes opContains or opNotContains search operator.


### -param ppIGPMGPOCollection [out]

Address of a pointer to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMGPOCollection</a> interface representing the GPOs found by the search.


#### - objGPMSearchCriteria


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> object to apply to the search.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">GPMGPOCollection</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">GPMGPOCollection</a> object.




## -remarks



An empty  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> object is one that has had no criteria added to it. Passing in an empty <b>GPMSearchCriteria</b> object will return all GPOs in the domain.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMGPOCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a>
 

 

