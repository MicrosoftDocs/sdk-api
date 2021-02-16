---
UID: NF:sdoias.ISdoDictionaryOld.EnumAttributeValues
title: ISdoDictionaryOld::EnumAttributeValues (sdoias.h)
description: The EnumAttributeValues method retrieves the values for an enumerable attribute.
helpviewer_keywords: ["EnumAttributeValues","EnumAttributeValues method [Network Policy Server]","EnumAttributeValues method [Network Policy Server]","ISdoDictionaryOld interface","ISdoDictionaryOld interface [Network Policy Server]","EnumAttributeValues method","ISdoDictionaryOld.EnumAttributeValues","ISdoDictionaryOld::EnumAttributeValues","_sdo_isdodictionaryold_enumattributevalues","nps.SDO_isdodictionaryold_enumattributevalues","sdo.isdodictionaryold_enumattributevalues","sdoias/ISdoDictionaryOld::EnumAttributeValues"]
old-location: nps\SDO_isdodictionaryold_enumattributevalues.htm
tech.root: Nps
ms.assetid: e46dc286-5316-49c2-a384-b486efc80d2a
ms.date: 12/05/2018
ms.keywords: EnumAttributeValues, EnumAttributeValues method [Network Policy Server], EnumAttributeValues method [Network Policy Server],ISdoDictionaryOld interface, ISdoDictionaryOld interface [Network Policy Server],EnumAttributeValues method, ISdoDictionaryOld.EnumAttributeValues, ISdoDictionaryOld::EnumAttributeValues, _sdo_isdodictionaryold_enumattributevalues, nps.SDO_isdodictionaryold_enumattributevalues, sdo.isdodictionaryold_enumattributevalues, sdoias/ISdoDictionaryOld::EnumAttributeValues
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
 - ISdoDictionaryOld::EnumAttributeValues
 - sdoias/ISdoDictionaryOld::EnumAttributeValues
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
 - ISdoDictionaryOld.EnumAttributeValues
---

# ISdoDictionaryOld::EnumAttributeValues


## -description

The 
<b>EnumAttributeValues</b> method retrieves the values for an enumerable attribute.

## -parameters

### -param Id [in]

Specifies the ID of the attribute.

### -param pValueIds [out]

On successful return points to a 
<a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> of value IDs for the enumerable attribute. If the attribute is not enumerable, points to a 
<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VT_EMPTY</a> variant.

### -param pValuesDesc [out]

On successful return points to a 
<a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> of value descriptions for the enumerable attribute. If the attribute is not enumerable, points to a 
<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VT_EMPTY</a> variant.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

The return value is S_OK even if the attribute is not enumerable.

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold">ISdoDictionaryOld</a>