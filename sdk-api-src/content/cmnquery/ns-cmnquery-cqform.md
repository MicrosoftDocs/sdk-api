---
UID: NS:cmnquery.CQFORM
title: CQFORM (cmnquery.h)
description: Used to define a query form added to the query dialog box with the CQAddFormsProc callback function.
helpviewer_keywords: ["*LPCQFORM","CQFF_ISOPTIONAL","CQFF_NOGLOBALPAGES","CQFORM","CQFORM structure [Active Directory]","LPCQFORM","LPCQFORM structure pointer [Active Directory]","_glines_cqform","ad.cqform","cmnquery/CQFORM","cmnquery/LPCQFORM"]
old-location: ad\cqform.htm
tech.root: ad
ms.assetid: 65cf2e9c-8f88-4e84-8bf2-2b0fd246a835
ms.date: 12/05/2018
ms.keywords: '*LPCQFORM, CQFF_ISOPTIONAL, CQFF_NOGLOBALPAGES, CQFORM, CQFORM structure [Active Directory], LPCQFORM, LPCQFORM structure pointer [Active Directory], _glines_cqform, ad.cqform, cmnquery/CQFORM, cmnquery/LPCQFORM'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CQFORM, *LPCQFORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPCQFORM
 - cmnquery/LPCQFORM
 - CQFORM
 - cmnquery/CQFORM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cmnquery.h
api_name:
 - CQFORM
---

# CQFORM structure


## -description

The <b>CQFORM</b> structure is used to define a query form added to the query dialog box with the <a href="/windows/desktop/api/cmnquery/nc-cmnquery-lpcqaddformsproc">CQAddFormsProc</a> callback function.

## -struct-fields

### -field cbStruct

Contains the size, in bytes, of the structure.

### -field dwFlags

Contains a set of flags that modify the behavior of the query form. This can be zero or a combination of one or more of the following values.



#### CQFF_ISOPTIONAL

Specifies that this query form is optional and is only displayed if optional forms are requested.



#### CQFF_NOGLOBALPAGES

Specifies that this form should not have the global pages added to it.

### -field clsid

Contains  the class identifier used to identify the query form.

### -field hIcon

Contains the  handle of the icon to be displayed with the query form.

### -field pszTitle

Pointer to a null-terminated Unicode string that contains the title of the query form.

## -see-also

<a href="/windows/desktop/api/cmnquery/nc-cmnquery-lpcqaddformsproc">CQAddFormsProc</a>



<a href="/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active
  Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-addforms">IQueryForm::AddForms</a>

