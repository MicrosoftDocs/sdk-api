---
UID: NF:sdoias.ISdo.get__NewEnum
title: ISdo::get__NewEnum (sdoias.h)
description: The get__NewEnum method retrieves an IEnumVARIANT interface for the Server Data Objects (SDO) properties.
helpviewer_keywords: ["ISdo interface [Network Policy Server]","get__NewEnum method","ISdo.get__NewEnum","ISdo::get__NewEnum","_sdo_isdo_get__newenum","get__NewEnum","get__NewEnum method [Network Policy Server]","get__NewEnum method [Network Policy Server]","ISdo interface","nps.SDO_isdo_get__newenum","sdo.isdo_get__newenum","sdoias/ISdo::get__NewEnum"]
old-location: nps\SDO_isdo_get__newenum.htm
tech.root: Nps
ms.assetid: 23033dc3-824c-429c-836d-65782ca3df92
ms.date: 12/05/2018
ms.keywords: ISdo interface [Network Policy Server],get__NewEnum method, ISdo.get__NewEnum, ISdo::get__NewEnum, _sdo_isdo_get__newenum, get__NewEnum, get__NewEnum method [Network Policy Server], get__NewEnum method [Network Policy Server],ISdo interface, nps.SDO_isdo_get__newenum, sdo.isdo_get__newenum, sdoias/ISdo::get__NewEnum
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISdo::get__NewEnum
 - sdoias/ISdo::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdo.get__NewEnum
---

# ISdo::get__NewEnum


## -description

The 
<b>get__NewEnum</b> method retrieves an 
<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface for the Server Data Objects (SDO) properties.

## -parameters

### -param ppEnumVARIANT [out]

Pointer to a pointer that, on successful return, points to an 
<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer. Use this <b>IUnknown</b> interface pointer with 
its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method to obtain an 
<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

<div class="alert"><b>Note</b>  Two underscores are used between "get" and "NewEnum" in the name of this method.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>



<a href="/windows/desktop/api/sdoias/nn-sdoias-isdo">ISdo</a>