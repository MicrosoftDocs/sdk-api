---
UID: NF:cmnquery.ICommonQuery.OpenQueryWindow
title: ICommonQuery::OpenQueryWindow
author: windows-sdk-content
description: The ICommonQuery::OpenQueryWindow method displays the directory service query dialog. This method does not return until the dialog box has been closed by the user.
old-location: ad\icommonquery_openquerywindow.htm
tech.root: ad
ms.assetid: 604c4d7a-1f85-4e5b-9879-be502c5c7bff
ms.author: windowssdkdev
ms.date: 11/14/2018
ms.keywords: CFSTR_DSOBJECTNAMES, CFSTR_DSQUERYPARAMS, CFSTR_DSQUERYSCOPE, ICommonQuery interface [Active Directory],OpenQueryWindow method, ICommonQuery.OpenQueryWindow, ICommonQuery::OpenQueryWindow, OpenQueryWindow, OpenQueryWindow method [Active Directory], OpenQueryWindow method [Active Directory],ICommonQuery interface, _glines_icommonquery_openquerywindow, ad.icommonquery__openquerywindow, ad.icommonquery_openquerywindow, cmnquery/ICommonQuery::OpenQueryWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cmnquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Dsquery.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsquery.dll
api_name:
 - ICommonQuery.OpenQueryWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cmnquery.h
: 
- ICommonQuery.OpenQueryWindow
: 
---

# ICommonQuery::OpenQueryWindow


## -description


The <b>ICommonQuery::OpenQueryWindow</b> method displays the directory service query dialog. This method does not return until the dialog box has been closed by the user.


## -parameters




### -param hwndParent

TBD


### -param pQueryWnd [in]

Address of an 
<a href="https://msdn.microsoft.com/07ef2af1-230e-41d9-ad19-d002d0579d66">OPENQUERYWINDOW</a> structure that defines the query to perform and the characteristics of the query dialog.


### -param ppDataObject

TBD




#### - hwdnParent [in]

Contains the handle of the window to use as the parent to the query dialog box. This parameter can be <b>NULL</b> if no parent is specified.


#### - ppDataObj [out]

Address of an <a href="_ole_idataobject">IDataObject</a> interface pointer that receives the results of the query. This parameter only receives valid data if this method returns <b>S_OK</b>. This <b>IDataObject</b> supports the following clipboard formats.



#### CFSTR_DSOBJECTNAMES

Contains data about  objects selected in the directory service query dialog box.



#### CFSTR_DSQUERYPARAMS

Contains data about the query performed by the directory service query dialog box.



#### CFSTR_DSQUERYSCOPE

Contains data about the scope of the query performed by the directory service query dialog box.


## -returns



Returns a standard <b>HRESULT</b> value including the following.




## -see-also




<a href="https://msdn.microsoft.com/b28428fa-1504-4dcc-9b2b-32ca1ae30ec5">CFSTR_DSOBJECTNAMES</a>



<a href="https://msdn.microsoft.com/bb8aea98-8309-42bf-993d-fa408bb4deb2">CFSTR_DSQUERYPARAMS</a>



<a href="https://msdn.microsoft.com/3cf51543-eca4-466c-bf0c-1351fd90798b">CFSTR_DSQUERYSCOPE</a>



<a href="https://msdn.microsoft.com/ff1cb792-efb0-46f5-bc9b-95c9fb2959db">DSQUERYINITPARAMS</a>



<a href="https://msdn.microsoft.com/78c3fb1c-275e-45b6-bbe9-ae2d85864e6a">DSQUERYPARAMS</a>



<a href="https://msdn.microsoft.com/f53d4425-5496-45f8-a09b-f163b63a29c8">Display Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/56d05afb-6e5e-41be-bc10-61192c1c1312">ICommonQuery</a>



<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/07ef2af1-230e-41d9-ad19-d002d0579d66">OPENQUERYWINDOW</a>
 

 

