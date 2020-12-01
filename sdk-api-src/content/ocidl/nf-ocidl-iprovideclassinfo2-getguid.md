---
UID: NF:ocidl.IProvideClassInfo2.GetGUID
title: IProvideClassInfo2::GetGUID (ocidl.h)
description: Retrieves the specified GUID for the object.
helpviewer_keywords: ["GetGUID","GetGUID method [COM]","GetGUID method [COM]","IProvideClassInfo2 interface","IProvideClassInfo2 interface [COM]","GetGUID method","IProvideClassInfo2.GetGUID","IProvideClassInfo2::GetGUID","_com_iprovideclassinfo2_getguid","com.iprovideclassinfo2_getguid","ocidl/IProvideClassInfo2::GetGUID"]
old-location: com\iprovideclassinfo2_getguid.htm
tech.root: com
ms.assetid: 1a424b93-93a9-4dc7-9c77-349522ee9e70
ms.date: 12/05/2018
ms.keywords: GetGUID, GetGUID method [COM], GetGUID method [COM],IProvideClassInfo2 interface, IProvideClassInfo2 interface [COM],GetGUID method, IProvideClassInfo2.GetGUID, IProvideClassInfo2::GetGUID, _com_iprovideclassinfo2_getguid, com.iprovideclassinfo2_getguid, ocidl/IProvideClassInfo2::GetGUID
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IProvideClassInfo2::GetGUID
 - ocidl/IProvideClassInfo2::GetGUID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IProvideClassInfo2.GetGUID
---

# IProvideClassInfo2::GetGUID


## -description

Retrieves the specified GUID for the object.

## -parameters

### -param dwGuidKind [in]

The GUID type. Possible values are from the <a href="/windows/desktop/api/ocidl/ne-ocidl-guidkind">GUIDKIND</a> enumeration.

### -param pGUID [out]

A pointer to a variable that receives the GUID.

## -returns

This method can return the standard return values E_INVALIDARG, E_UNEXPECTED, E_POINTER, and S_OK.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo2">IProvideClassInfo2</a>