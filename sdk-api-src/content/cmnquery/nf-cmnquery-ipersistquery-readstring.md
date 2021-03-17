---
UID: NF:cmnquery.IPersistQuery.ReadString
title: IPersistQuery::ReadString (cmnquery.h)
description: Reads a string from the query store.
helpviewer_keywords: ["IPersistQuery interface [Active Directory]","ReadString method","IPersistQuery.ReadString","IPersistQuery::ReadString","ReadString","ReadString method [Active Directory]","ReadString method [Active Directory]","IPersistQuery interface","_glines_ipersistquery_readstring","ad.ipersistquery__readstring","ad.ipersistquery_readstring","cmnquery/IPersistQuery::ReadString"]
old-location: ad\ipersistquery_readstring.htm
tech.root: ad
ms.assetid: 5d96234f-080e-49c6-ae31-c4eb672ecf04
ms.date: 12/05/2018
ms.keywords: IPersistQuery interface [Active Directory],ReadString method, IPersistQuery.ReadString, IPersistQuery::ReadString, ReadString, ReadString method [Active Directory], ReadString method [Active Directory],IPersistQuery interface, _glines_ipersistquery_readstring, ad.ipersistquery__readstring, ad.ipersistquery_readstring, cmnquery/IPersistQuery::ReadString
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
 - IPersistQuery::ReadString
 - cmnquery/IPersistQuery::ReadString
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
 - IPersistQuery.ReadString
---

# IPersistQuery::ReadString


## -description

The <b>IPersistQuery::ReadString</b> method reads a string from the query store.

## -parameters

### -param pSection [in]

Pointer to a null-terminated Unicode string that represents the section name that the string should be read from.

### -param pValueName [in]

Pointer to a null-terminated Unicode string that represents the name of the string value to be read.

### -param pBuffer [out]

Pointer to a character buffer that receives the string value. The <i>cchBuffer</i> parameter specifies the size of this buffer including the null terminator.

### -param cchBuffer [in]

Contains the size, in characters, of the <i>pBuffer</i> buffer including the null terminator.

## -returns

Returns <b>S_OK</b> if successful or a standard  <b>HRESULT</b> value otherwise. Possible error codes include the following.

## -see-also

<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a>