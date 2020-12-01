---
UID: NF:cmnquery.IPersistQuery.WriteStruct
title: IPersistQuery::WriteStruct (cmnquery.h)
description: Writes a structure to the query store.
helpviewer_keywords: ["IPersistQuery interface [Active Directory]","WriteStruct method","IPersistQuery.WriteStruct","IPersistQuery::WriteStruct","WriteStruct","WriteStruct method [Active Directory]","WriteStruct method [Active Directory]","IPersistQuery interface","_glines_ipersistquery_writestruct","ad.ipersistquery__writestruct","ad.ipersistquery_writestruct","cmnquery/IPersistQuery::WriteStruct"]
old-location: ad\ipersistquery_writestruct.htm
tech.root: ad
ms.assetid: c0acd6c7-96ee-4650-9cfc-3bad4fdffdcc
ms.date: 12/05/2018
ms.keywords: IPersistQuery interface [Active Directory],WriteStruct method, IPersistQuery.WriteStruct, IPersistQuery::WriteStruct, WriteStruct, WriteStruct method [Active Directory], WriteStruct method [Active Directory],IPersistQuery interface, _glines_ipersistquery_writestruct, ad.ipersistquery__writestruct, ad.ipersistquery_writestruct, cmnquery/IPersistQuery::WriteStruct
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
 - IPersistQuery::WriteStruct
 - cmnquery/IPersistQuery::WriteStruct
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
 - IPersistQuery.WriteStruct
---

# IPersistQuery::WriteStruct


## -description

The <b>IPersistQuery::WriteStruct</b> method writes a structure to the query store.

## -parameters

### -param pSection [in]

Pointer to a null-terminated Unicode string that represents the section name that the structure should be written to.

### -param pValueName [in]

Pointer to a null-terminated Unicode string that represents the name of the structure.

### -param pStruct [in]

Pointer to the structure to be written. The <i>cbStruct</i> parameter contains the number of bytes to be written.

### -param cbStruct [in]

Contains the size, in bytes, of the structure to be written.

## -returns

Returns <b>S_OK</b> if successful or a standard  <b>HRESULT</b> value otherwise. Possible error codes include the following.

## -see-also

<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a>