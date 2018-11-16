---
UID: NF:gpmgmt.IGPMDomain2.SearchStarterGPOs
title: IGPMDomain2::SearchStarterGPOs
author: windows-sdk-content
description: Executes a search for GPMStarterGPO objects.
old-location: gpmc\igpmdomain2_searchstartergpos.htm
tech.root: GPMC
ms.assetid: 30a325e8-372a-4e30-a420-10f5b6ef295d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IGPMDomain2 interface [GPMC],SearchStarterGPOs method, IGPMDomain2.SearchStarterGPOs, IGPMDomain2::SearchStarterGPOs, SearchStarterGPOs, SearchStarterGPOs method [GPMC], SearchStarterGPOs method [GPMC],IGPMDomain2 interface, gpmc.igpmdomain2_searchstartergpos, gpmgmt/IGPMDomain2::SearchStarterGPOs, starterGPODisplayName, starterGPOEffectivePermissions, starterGPOID, starterGPOPermissions
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
 - gpmgmt.dll
api_name:
 - IGPMDomain2.SearchStarterGPOs
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
- IGPMDomain2.SearchStarterGPOs
: 
---

# IGPMDomain2::SearchStarterGPOs


## -description


Executes a search for 
<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">GPMStarterGPO</a> objects  in the domain and returns a 
<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">GPMStarterGPOCollection</a> object.


## -parameters




### -param pIGPMSearchCriteria [in]

Pointer to the criteria to apply to the search.



#### starterGPODisplayName

Pointer to  the friendly Starter Group Policy object (GPO) display name search. The search property value is the Starter GPO display name. The valid criteria include the <b>opEquals</b>, 
<b>opContains</b>, and <b>opNotContains</b> search operators.



#### starterGPOPermissions

Pointer to an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> or <a href="_com_iunknown">IUnknown</a> interface to query the <a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">IGPMPermission</a> interface. For script programmers, his is a reference to a <b>GPMPermission</b> object. The valid criteria include the <b>opContains</b> or <b>opNotContains</b> search operators.



#### starterGPOEffectivePermissions

Pointer to an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> or <a href="_com_iunknown">IUnknown</a> interface to query the 
<a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">IGPMPermission</a> interface. The valid criteria include the <b>opContains</b> and <b>opNotContains</b> search operators.



#### starterGPOID

Pointer to a string that contains a GUID. The GUID represents the ID of the Starter GPO. The valid criteria include the <b>opEquals</b> and <b>opNotEquals</b> search operators.


### -param ppIGPMTemplateCollection [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/b650b1c6-0597-468a-afdc-a21d61f1a8a0">IGPMStarterGPOCollection</a> interface that represents the GPOs found by the search.


#### - objGPMSearchCriteria


<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">GPMSearchCriteria</a> object to apply to the search.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a  <a href="https://msdn.microsoft.com/b650b1c6-0597-468a-afdc-a21d61f1a8a0">GPMStarterGPOCollection</a> object.

<h3>VB</h3>
Returns a reference to a  <a href="https://msdn.microsoft.com/b650b1c6-0597-468a-afdc-a21d61f1a8a0">GPMStarterGPOCollection</a> object.




## -see-also




<a href="https://msdn.microsoft.com/5abfea14-0cb9-46ea-915c-93a8d8b2477b">IGPMDomain2</a>
 

 

