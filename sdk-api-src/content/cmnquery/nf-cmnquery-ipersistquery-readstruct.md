---
UID: NF:cmnquery.IPersistQuery.ReadStruct
title: IPersistQuery::ReadStruct (cmnquery.h)
description: Reads a structure from the query store.
helpviewer_keywords: ["IPersistQuery interface [Active Directory]","ReadStruct method","IPersistQuery.ReadStruct","IPersistQuery::ReadStruct","ReadStruct","ReadStruct method [Active Directory]","ReadStruct method [Active Directory]","IPersistQuery interface","_glines_ipersistquery_readstruct","ad.ipersistquery__readstruct","ad.ipersistquery_readstruct","cmnquery/IPersistQuery::ReadStruct"]
old-location: ad\ipersistquery_readstruct.htm
tech.root: ad
ms.assetid: 47d1b733-7e37-42f8-b344-909a6e48b381
ms.date: 12/05/2018
ms.keywords: IPersistQuery interface [Active Directory],ReadStruct method, IPersistQuery.ReadStruct, IPersistQuery::ReadStruct, ReadStruct, ReadStruct method [Active Directory], ReadStruct method [Active Directory],IPersistQuery interface, _glines_ipersistquery_readstruct, ad.ipersistquery__readstruct, ad.ipersistquery_readstruct, cmnquery/IPersistQuery::ReadStruct
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
 - IPersistQuery::ReadStruct
 - cmnquery/IPersistQuery::ReadStruct
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
 - IPersistQuery.ReadStruct
---

# IPersistQuery::ReadStruct


## -description

The <b>IPersistQuery::ReadStruct</b> method reads a structure from the query store.

## -parameters

### -param pSection [in]

Pointer to a null-terminated Unicode string that represents the section name that the structure should be read from.

### -param pValueName [in]

Pointer to a null-terminated Unicode string that represents the name of the structure value to be read.

### -param pStruct [out]

Pointer to a buffer that will receive the structure. The <i>cbStruct</i> parameter specifies the size of this buffer, in bytes.

### -param cbStruct [in]

Specifies the size, in bytes, of the  buffer represented by the <i>pStruct</i> parameter.

## -returns

Returns <b>S_OK</b> if successful or a standard  <b>HRESULT</b> value otherwise. Possible error codes include the following.

## -see-also

<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a>