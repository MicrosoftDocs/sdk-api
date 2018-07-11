---
UID: NF:gpmgmt.IGPMDomain.SearchGPOs
title: IGPMDomain::SearchGPOs
author: windows-sdk-content
description: Executes a search for GPMGPO objects in the domain and then returns a GPMGPOCollection object.
old-location: gpmc\igpmdomain_searchgpos.htm
old-project: gpmc
ms.assetid: 19a8efae-0b85-49ba-bf7e-08ed700874c3
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: GPMDomain object [GPMC],SearchGPOs method, IGPMDomain interface [GPMC],SearchGPOs method, IGPMDomain.SearchGPOs, IGPMDomain::SearchGPOs, SearchGPOs, SearchGPOs method [GPMC], SearchGPOs method [GPMC],GPMDomain object, SearchGPOs method [GPMC],IGPMDomain interface, _win32_igpmdomain_searchgpos, gpmc.igpmdomain_searchgpos, gpmgmt/IGPMDomain::SearchGPOs, gpoComputerExtensions, gpoDisplayName, gpoEffectivePermissions, gpoID, gpoPermissions, gpoUserExtensions, gpoWMIFilter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: GPMStarterGPOType
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
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMDomain::SearchGPOs


## -description


Executes a search for 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> objects in the domain and then returns a 
<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">GPMGPOCollection</a> object.


## -parameters




### -param pIGPMSearchCriteria [in]

Pointer to the criteria to apply to the search.



#### gpoDisplayName

Pointer to a  friendly Group Policy object (GPO) display name search. The search property value is the friendly GPO display name. Valid criteria include the <b>opEquals</b>, 
<b>opContains</b>, and <b>opNotContains</b> search operators.



#### gpoPermissions

Pointer to an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> or <a href="_com_iunknown">IUnknown</a> interface to query the <a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">IGPMPermission</a> interface. For script programmers, this is a reference to a <b>GPMPermission</b> object. Valid criteria include the <b>opContains</b> and <b>opNotContains</b> search operators.



#### gpoEffectivePermissions

Pointer to an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> or an <a href="_com_iunknown">IUnknown</a> interface to query the 
<a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">IGPMPermission</a> interface. Valid criteria includes opContains or opNotContains search operator.



#### gpoWMIFilter

Pointer to an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> or an <a href="_com_iunknown">IUnknown</a> interface to query the 
<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a> interface. Valid criteria includes opEquals or opNotEquals search operator.



#### gpoID

Pointer to a string containing a GUID that represents the group policy object's ID. Valid criteria includes opEquals or opNotEquals search operator.



#### gpoComputerExtensions

Pointer to a string containing a GUID that represents the client-side extension's ID. Valid criteria includes opContains or opNotContains search operator.



#### gpoUserExtensions

Pointer to a string containing a GUID that represents the user extension's ID.
 Valid criteria includes opContains or opNotContains search operator.


### -param ppIGPMGPOCollection [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">IGPMGPOCollection</a> interface representing the GPOs found by the search.


#### - objGPMSearchCriteria


<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">GPMSearchCriteria</a> object to apply to the search.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">GPMGPOCollection</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">GPMGPOCollection</a> object.




## -remarks



An empty  <a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">GPMSearchCriteria</a> object is one that has had no criteria added to it. Passing in an empty <b>GPMSearchCriteria</b> object will return all GPOs in the domain.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">IGPMGPOCollection</a>



<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">IGPMSearchCriteria</a>
 

 

