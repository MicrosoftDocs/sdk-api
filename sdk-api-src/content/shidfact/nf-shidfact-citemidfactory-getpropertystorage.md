---
UID: NF:shidfact.CItemIDFactory.GetPropertyStorage
title: CItemIDFactory::GetPropertyStorage (shidfact.h)
description: Gets a read only pointer to the serialized property storage that is used for storing metadata.
helpviewer_keywords: ["CItemIDFactory interface [Windows Shell]","GetPropertyStorage method","CItemIDFactory.GetPropertyStorage","CItemIDFactory::GetPropertyStorage","GetPropertyStorage","GetPropertyStorage method [Windows Shell]","GetPropertyStorage method [Windows Shell]","CItemIDFactory interface","shell.citemidfactory_getpropertystorage","shidfact/CItemIDFactory::GetPropertyStorage"]
old-location: shell\citemidfactory_getpropertystorage.htm
tech.root: shell
ms.assetid: 3A3F0F28-C9E1-4F2E-9A02-C6A48BF3C204
ms.date: 12/05/2018
ms.keywords: CItemIDFactory interface [Windows Shell],GetPropertyStorage method, CItemIDFactory.GetPropertyStorage, CItemIDFactory::GetPropertyStorage, GetPropertyStorage, GetPropertyStorage method [Windows Shell], GetPropertyStorage method [Windows Shell],CItemIDFactory interface, shell.citemidfactory_getpropertystorage, shidfact/CItemIDFactory::GetPropertyStorage
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
 - CItemIDFactory::GetPropertyStorage
 - shidfact/CItemIDFactory::GetPropertyStorage
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
 - CItemIDFactory.GetPropertyStorage
---

# CItemIDFactory::GetPropertyStorage


## -description

Gets  a read only pointer to the serialized property storage that is used for storing metadata.

## -parameters

### -param pidl [in, optional]

A PIDL that contains the location of the property storage.

### -param pcb [out]

When this method returns, contains the size, in bytes, of the storage.

## -returns

If this method succeeds, it returns a read only pointer to the serialized property storage.

## -see-also

<a href="/windows/desktop/api/shidfact/nl-shidfact-citemidfactory">CItemIDFactory</a>