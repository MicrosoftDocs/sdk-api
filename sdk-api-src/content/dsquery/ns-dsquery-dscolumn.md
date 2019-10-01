---
UID: NS:dsquery.__unnamed_struct_1
title: DSCOLUMN (dsquery.h)
author: windows-sdk-content
description: The DSCOLUMN structure represents a column in the directory services query dialog box. An array of this structure is contained in the DSQUERYPARAMS structure.
old-location: ad\dscolumn.htm
tech.root: ad
ms.assetid: b948b114-dd66-4e79-bdd0-559a13a7c644
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDSCOLUMN, DSCOLUMN, DSCOLUMN structure [Active Directory], DSCOLUMNPROP_ADSPATH, DSCOLUMNPROP_OBJECTCLASS, LPDSCOLUMN, LPDSCOLUMN structure pointer [Active Directory], _glines_dscolumn, ad.dscolumn, dsquery/DSCOLUMN, dsquery/LPDSCOLUMN"
ms.topic: struct
f1_keywords: 
 - "dsquery/DSCOLUMN"
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
 - DSCOLUMN
targetos: Windows
req.typenames: DSCOLUMN, *LPDSCOLUMN
req.redist: 
ms.custom: 19H1
---

# DSCOLUMN structure


## -description


The <b>DSCOLUMN</b> structure represents a column in the directory services query dialog box. An array of this structure is contained in the <a href="https://docs.microsoft.com/windows/desktop/api/dsquery/ns-dsquery-dsqueryparams">DSQUERYPARAMS</a> structure.


## -struct-fields




### -field dwFlags

Reserved.


### -field fmt

Contains one of the list view column formatting values that indicates how the column is displayed. The possible values are defined for the <b>fmt</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvcolumna">LVCOLUMN</a> structure.


### -field cx

Contains the width, in pixels, of the column.


### -field idsName

Contains the string table identifier for the column header string. To retrieve this string, call  <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a> with the <b>hInstance</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/dsquery/ns-dsquery-dsqueryparams">DSQUERYPARAMS</a> structure and this member for the string identifier.


### -field offsetProperty

Indicates the name of the attribute displayed in the column. This can be one of the following values.



#### DSCOLUMNPROP_ADSPATH

The column displays the value of the ADsPath of the object.



#### DSCOLUMNPROP_OBJECTCLASS

The column displays the value of the <b>objectClass</b> of the object.

If this member does not contain one of these values, this member contains the offset, in bytes, from the address of the <a href="https://docs.microsoft.com/windows/desktop/api/dsquery/ns-dsquery-dsqueryparams">DSQUERYPARAMS</a> structure to a null-terminated  Unicode string that contains the name of the  attribute value displayed in this column.


### -field dwReserved

Reserved.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dsquery/ns-dsquery-dsqueryparams">DSQUERYPARAMS</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active Directory Domain Services</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvcolumna">LVCOLUMN</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a>
 

 

