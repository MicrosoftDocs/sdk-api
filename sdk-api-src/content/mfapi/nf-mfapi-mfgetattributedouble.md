---
UID: NF:mfapi.MFGetAttributeDouble
title: MFGetAttributeDouble function (mfapi.h)
description: Returns a double value from an attribute store, or a default value if the attribute is not present.
helpviewer_keywords: ["61a9e327-da29-45fd-8a99-e341561826af","MFGetAttributeDouble","MFGetAttributeDouble function [Media Foundation]","mf.mfgetattributedouble","mfapi/MFGetAttributeDouble"]
old-location: mf\mfgetattributedouble.htm
tech.root: mf
ms.assetid: 61a9e327-da29-45fd-8a99-e341561826af
ms.date: 12/05/2018
ms.keywords: 61a9e327-da29-45fd-8a99-e341561826af, MFGetAttributeDouble, MFGetAttributeDouble function [Media Foundation], mf.mfgetattributedouble, mfapi/MFGetAttributeDouble
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFGetAttributeDouble
 - mfapi/MFGetAttributeDouble
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFGetAttributeDouble
---

# MFGetAttributeDouble function


## -description

Returns a <b>double</b> value from an attribute store, or a default value if the attribute is not present.

## -parameters

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.

### -param guidKey [in]

GUID that identifies which value to retrieve.

### -param fDefault [in]

Default value to return if the attribute store does not contain the specified attribute.

## -returns

Returns a <b>double</b> value.

## -remarks

This helper function queries the attribute store for the attribute specified by <i>guidKey</i>. If the attribute is not present or does not have type <b>double</b>, the function returns <i>fDefault</i>.

This function is convenient because it never returns a failure code. However, if the attribute in question does not have a meaningful default value, you should call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getdouble">IMFAttributes::GetDouble</a> and check for MF_E_ATTRIBUTENOTFOUND.

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getdouble">IMFAttributes::GetDouble</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>