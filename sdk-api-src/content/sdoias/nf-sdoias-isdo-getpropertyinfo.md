---
UID: NF:sdoias.ISdo.GetPropertyInfo
title: ISdo::GetPropertyInfo (sdoias.h)
description: The GetPropertyInfo method retrieves a pointer to an ISdoPropertyInfo interface for the specified property.
helpviewer_keywords: ["GetPropertyInfo","GetPropertyInfo method [Network Policy Server]","GetPropertyInfo method [Network Policy Server]","ISdo interface","ISdo interface [Network Policy Server]","GetPropertyInfo method","ISdo.GetPropertyInfo","ISdo::GetPropertyInfo","_sdo_isdo_getpropertyinfo","nps.SDO_isdo_getpropertyinfo","sdo.isdo_getpropertyinfo","sdoias/ISdo::GetPropertyInfo"]
old-location: nps\SDO_isdo_getpropertyinfo.htm
tech.root: Nps
ms.assetid: fa2f0209-ec78-4b59-8f01-f1534b8894c1
ms.date: 12/05/2018
ms.keywords: GetPropertyInfo, GetPropertyInfo method [Network Policy Server], GetPropertyInfo method [Network Policy Server],ISdo interface, ISdo interface [Network Policy Server],GetPropertyInfo method, ISdo.GetPropertyInfo, ISdo::GetPropertyInfo, _sdo_isdo_getpropertyinfo, nps.SDO_isdo_getpropertyinfo, sdo.isdo_getpropertyinfo, sdoias/ISdo::GetPropertyInfo
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
 - ISdo::GetPropertyInfo
 - sdoias/ISdo::GetPropertyInfo
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
 - ISdo.GetPropertyInfo
---

# ISdo::GetPropertyInfo


## -description

The 
<b>GetPropertyInfo</b> method retrieves a pointer to an <b>ISdoPropertyInfo</b> interface for the specified property.

<b>Warning:  </b>The <b>ISdoPropertyInfo</b> interface is unsupported and the use of this method to access it is discouraged.

## -parameters

### -param Id [in]

Specifies the ID of an existing property.

### -param ppPropertyInfo [out]

Pointer to a pointer that receives the address of an <b>ISdoPropertyInfo</b> interface for the specified property.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

Although Server Data Objects (SDO) exposes this method, you do not need it in order to use SDO.

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdo">ISdo</a>