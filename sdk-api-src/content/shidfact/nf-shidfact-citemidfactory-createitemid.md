---
UID: NF:shidfact.CItemIDFactory.CreateItemID
title: CItemIDFactory::CreateItemID (shidfact.h)
description: Creates an ItemID from the supplied data.
helpviewer_keywords: ["CItemIDFactory interface [Windows Shell]","CreateItemID method","CItemIDFactory.CreateItemID","CItemIDFactory::CreateItemID","CreateItemID","CreateItemID method [Windows Shell]","CreateItemID method [Windows Shell]","CItemIDFactory interface","shell.citemidfactory_createitemid","shidfact/CItemIDFactory::CreateItemID"]
old-location: shell\citemidfactory_createitemid.htm
tech.root: shell
ms.assetid: 2129F4F3-A989-4CE2-ABFF-FE83DD78D4CE
ms.date: 12/05/2018
ms.keywords: CItemIDFactory interface [Windows Shell],CreateItemID method, CItemIDFactory.CreateItemID, CItemIDFactory::CreateItemID, CreateItemID, CreateItemID method [Windows Shell], CreateItemID method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_createitemid, shidfact/CItemIDFactory::CreateItemID
req.header: shidfact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CItemIDFactory::CreateItemID
 - shidfact/CItemIDFactory::CreateItemID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shidfact.h
api_name:
 - CItemIDFactory.CreateItemID
---

# CItemIDFactory::CreateItemID


## -description

Creates an ItemID from the supplied data.

## -parameters

### -param pinner [in, optional]

A pointer to the client structure that should be copied.

### -param pps [in, out, optional]

A pointer to an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> that will be seriallized into the ItemID.

### -param ppidl [out]

When this method returns, contains a pointer to the ItemID containing the client data and <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The size of the user supplied data must equal sizeof(T). Do not use structs with variably allocated array/string members. The struct must also follow standard <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> for persistence and portability.

## -see-also

<a href="/windows/desktop/api/shidfact/nl-shidfact-citemidfactory">CItemIDFactory</a>



<a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>



<a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a>