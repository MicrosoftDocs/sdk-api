---
UID: NF:gpmgmt.IGPMDomain2.SearchStarterGPOs
title: IGPMDomain2::SearchStarterGPOs (gpmgmt.h)
description: Executes a search for GPMStarterGPO objects.
old-location: gpmc\igpmdomain2_searchstartergpos.htm
tech.root: gpmc
ms.assetid: 30a325e8-372a-4e30-a420-10f5b6ef295d
ms.date: 12/05/2018
ms.keywords: IGPMDomain2 interface [GPMC],SearchStarterGPOs method, IGPMDomain2.SearchStarterGPOs, IGPMDomain2::SearchStarterGPOs, SearchStarterGPOs, SearchStarterGPOs method [GPMC], SearchStarterGPOs method [GPMC],IGPMDomain2 interface, gpmc.igpmdomain2_searchstartergpos, gpmgmt/IGPMDomain2::SearchStarterGPOs, starterGPODisplayName, starterGPOEffectivePermissions, starterGPOID, starterGPOPermissions
ms.topic: method
f1_keywords:
- gpmgmt/IGPMDomain2.SearchStarterGPOs
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
- gpmgmt.dll
api_name:
- IGPMDomain2.SearchStarterGPOs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMDomain2::SearchStarterGPOs


## -description


Executes a search for 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a> objects  in the domain and returns a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">GPMStarterGPOCollection</a> object.


## -parameters




### -param pIGPMSearchCriteria [in]

Pointer to the criteria to apply to the search.



#### starterGPODisplayName

Pointer to  the friendly Starter Group Policy object (GPO) display name search. The search property value is the Starter GPO display name. The valid criteria include the <b>opEquals</b>, 
<b>opContains</b>, and <b>opNotContains</b> search operators.



#### starterGPOPermissions

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> or <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface to query the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a> interface. For script programmers, his is a reference to a <b>GPMPermission</b> object. The valid criteria include the <b>opContains</b> or <b>opNotContains</b> search operators.



#### starterGPOEffectivePermissions

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> or <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface to query the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a> interface. The valid criteria include the <b>opContains</b> and <b>opNotContains</b> search operators.



#### starterGPOID

Pointer to a string that contains a GUID. The GUID represents the ID of the Starter GPO. The valid criteria include the <b>opEquals</b> and <b>opNotEquals</b> search operators.


### -param ppIGPMTemplateCollection [out]

Address of a pointer to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpocollection">IGPMStarterGPOCollection</a> interface that represents the GPOs found by the search.


#### - objGPMSearchCriteria


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> object to apply to the search.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpocollection">GPMStarterGPOCollection</a> object.

<h3>VB</h3>
Returns a reference to a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpocollection">GPMStarterGPOCollection</a> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain2">IGPMDomain2</a>
 

 

