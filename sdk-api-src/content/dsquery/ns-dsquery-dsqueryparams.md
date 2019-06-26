---
UID: NS:dsquery.__unnamed_struct_2
title: DSQUERYPARAMS (dsquery.h)
author: windows-sdk-content
description: The DSQUERYPARAMS structure contains query data used by the directory service query when searching the directory service.
old-location: ad\dsqueryparams.htm
tech.root: ad
ms.assetid: 78c3fb1c-275e-45b6-bbe9-ae2d85864e6a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDSQUERYPARAMS, DSQUERYPARAMS, DSQUERYPARAMS structure [Active Directory], LPDSQUERYPARAMS, LPDSQUERYPARAMS structure pointer [Active Directory], _glines_dsqueryparams, ad.dsqueryparams, dsquery/DSQUERYPARAMS, dsquery/LPDSQUERYPARAMS"
ms.topic: struct
f1_keywords: 
 - "dsquery/DSQUERYPARAMS"
req.header: dsquery.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsquery.h
api_name:
 - DSQUERYPARAMS
product: Windows
targetos: Windows
req.typenames: DSQUERYPARAMS, *LPDSQUERYPARAMS
req.redist: 
ms.custom: 19H1
---

# DSQUERYPARAMS structure


## -description


The <b>DSQUERYPARAMS</b> structure contains query  data used by the directory service query when searching the directory service. This structure is provided by the <a href="https://docs.microsoft.com/windows/desktop/AD/cfstr-dsqueryparams">CFSTR_DSQUERYPARAMS</a> clipboard format by the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> provided by the <a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a> method. The caller of <b>ICommonQuery::OpenQueryWindow</b> can use this to retrieve the filter, column data used by the result view when issuing a query against the server.


## -struct-fields




### -field cbStruct

Contains the size, in bytes, of the <b>DSQUERYPARAMS</b> structure. This member is used for versioning of the structure.


### -field dwFlags

Reserved.


### -field hInstance

Contains an instance handle used for extracting resources.


### -field offsetQuery

Contains the offset, in bytes,  from the address of this structure to a null-terminated Unicode string that contains the  LDAP filter.


### -field iColumns

Contains the number of elements in the <b>aColumns</b> array.


### -field dwReserved

Reserved.


### -field aColumns

Contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/dsquery/ns-dsquery-dscolumn">DSCOLUMN</a> structures that contain the results of the query. The <b>iColumns</b> member specifies the number of elements in this array.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/cfstr-dsqueryparams">CFSTR_DSQUERYPARAMS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsquery/ns-dsquery-dscolumn">DSCOLUMN</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active Directory Domain Services</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a>
 

 

