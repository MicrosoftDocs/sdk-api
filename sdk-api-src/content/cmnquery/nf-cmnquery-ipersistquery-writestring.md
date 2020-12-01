---
UID: NF:cmnquery.IPersistQuery.WriteString
title: IPersistQuery::WriteString (cmnquery.h)
description: Writes a string to the query store.
helpviewer_keywords: ["IPersistQuery interface [Active Directory]","WriteString method","IPersistQuery.WriteString","IPersistQuery::WriteString","WriteString","WriteString method [Active Directory]","WriteString method [Active Directory]","IPersistQuery interface","_glines_ipersistquery_writestring","ad.ipersistquery__writestring","ad.ipersistquery_writestring","cmnquery/IPersistQuery::WriteString"]
old-location: ad\ipersistquery_writestring.htm
tech.root: ad
ms.assetid: 6bf8499a-6b3a-4786-8d42-67ab4e1a40c0
ms.date: 12/05/2018
ms.keywords: IPersistQuery interface [Active Directory],WriteString method, IPersistQuery.WriteString, IPersistQuery::WriteString, WriteString, WriteString method [Active Directory], WriteString method [Active Directory],IPersistQuery interface, _glines_ipersistquery_writestring, ad.ipersistquery__writestring, ad.ipersistquery_writestring, cmnquery/IPersistQuery::WriteString
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPersistQuery::WriteString
 - cmnquery/IPersistQuery::WriteString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsquery.dll
api_name:
 - IPersistQuery.WriteString
---

# IPersistQuery::WriteString


## -description

The <b>IPersistQuery::WriteString</b> method writes a string to the query store.

## -parameters

### -param pSection [in]

Pointer to a null-terminated Unicode string that represents the section name that the string should be written to.

### -param pValueName [in]

Pointer to a null-terminated Unicode string that represents the name of the string value.

### -param pValue [in]

Pointer to a null-terminated Unicode string that contains the string to be written.

## -returns

Returns <b>S_OK</b> if successful or a standard  <b>HRESULT</b> value otherwise. Possible error codes include the following.

## -see-also

<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a>