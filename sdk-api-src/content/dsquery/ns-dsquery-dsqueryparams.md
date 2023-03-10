---
UID: NS:dsquery.DSQUERYPARAMS
title: DSQUERYPARAMS (dsquery.h)
description: The DSQUERYPARAMS structure contains query data used by the directory service query when searching the directory service.
helpviewer_keywords: ["*LPDSQUERYPARAMS","DSQUERYPARAMS","DSQUERYPARAMS structure [Active Directory]","LPDSQUERYPARAMS","LPDSQUERYPARAMS structure pointer [Active Directory]","_glines_dsqueryparams","ad.dsqueryparams","dsquery/DSQUERYPARAMS","dsquery/LPDSQUERYPARAMS"]
old-location: ad\dsqueryparams.htm
tech.root: ad
ms.assetid: 78c3fb1c-275e-45b6-bbe9-ae2d85864e6a
ms.date: 12/05/2018
ms.keywords: '*LPDSQUERYPARAMS, DSQUERYPARAMS, DSQUERYPARAMS structure [Active Directory], LPDSQUERYPARAMS, LPDSQUERYPARAMS structure pointer [Active Directory], _glines_dsqueryparams, ad.dsqueryparams, dsquery/DSQUERYPARAMS, dsquery/LPDSQUERYPARAMS'
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
targetos: Windows
req.typenames: DSQUERYPARAMS, *LPDSQUERYPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDSQUERYPARAMS
 - dsquery/LPDSQUERYPARAMS
 - DSQUERYPARAMS
 - dsquery/DSQUERYPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsquery.h
api_name:
 - DSQUERYPARAMS
---

# DSQUERYPARAMS structure


## -description

The <b>DSQUERYPARAMS</b> structure contains query  data used by the directory service query when searching the directory service. This structure is provided by the <a href="/windows/desktop/AD/cfstr-dsqueryparams">CFSTR_DSQUERYPARAMS</a> clipboard format by the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> provided by the <a href="/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a> method. The caller of <b>ICommonQuery::OpenQueryWindow</b> can use this to retrieve the filter, column data used by the result view when issuing a query against the server.

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

Contains an array of <a href="/windows/desktop/api/dsquery/ns-dsquery-dscolumn">DSCOLUMN</a> structures that contain the results of the query. The <b>iColumns</b> member specifies the number of elements in this array.

## -see-also

<a href="/windows/desktop/AD/cfstr-dsqueryparams">CFSTR_DSQUERYPARAMS</a>



<a href="/windows/desktop/api/dsquery/ns-dsquery-dscolumn">DSCOLUMN</a>



<a href="/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a>

