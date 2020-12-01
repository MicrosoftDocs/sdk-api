---
UID: NF:cmnquery.IPersistQuery.WriteInt
title: IPersistQuery::WriteInt (cmnquery.h)
description: Writes an integer value to the query store.
helpviewer_keywords: ["IPersistQuery interface [Active Directory]","WriteInt method","IPersistQuery.WriteInt","IPersistQuery::WriteInt","WriteInt","WriteInt method [Active Directory]","WriteInt method [Active Directory]","IPersistQuery interface","_glines_ipersistquery_writeint","ad.ipersistquery__writeint","ad.ipersistquery_writeint","cmnquery/IPersistQuery::WriteInt"]
old-location: ad\ipersistquery_writeint.htm
tech.root: ad
ms.assetid: 5f68865a-dd9f-4428-9cbc-f998f0f1f4a7
ms.date: 12/05/2018
ms.keywords: IPersistQuery interface [Active Directory],WriteInt method, IPersistQuery.WriteInt, IPersistQuery::WriteInt, WriteInt, WriteInt method [Active Directory], WriteInt method [Active Directory],IPersistQuery interface, _glines_ipersistquery_writeint, ad.ipersistquery__writeint, ad.ipersistquery_writeint, cmnquery/IPersistQuery::WriteInt
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
 - IPersistQuery::WriteInt
 - cmnquery/IPersistQuery::WriteInt
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
 - IPersistQuery.WriteInt
---

# IPersistQuery::WriteInt


## -description

The <b>IPersistQuery::WriteInt</b> method writes an integer value to the query store.

## -parameters

### -param pSection [in]

Pointer to a null-terminated Unicode string that represents the section name that the integer should be written to.

### -param pValueName [in]

Pointer to a null-terminated Unicode string that represents the name of the integer value.

### -param value [in]

Contains the integer value to be written to the query store.

## -returns

Returns <b>S_OK</b> if successful or a standard  <b>HRESULT</b> value otherwise. Possible error codes include the following.

## -see-also

<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a>