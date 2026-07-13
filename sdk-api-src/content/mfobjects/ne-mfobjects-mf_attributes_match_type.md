---
UID: NE:mfobjects._MF_ATTRIBUTES_MATCH_TYPE
title: MF_ATTRIBUTES_MATCH_TYPE (mfobjects.h)
description: Specifies how to compare the attributes on two objects.
helpviewer_keywords: ["MF_ATTRIBUTES_MATCH_ALL_ITEMS","MF_ATTRIBUTES_MATCH_INTERSECTION","MF_ATTRIBUTES_MATCH_OUR_ITEMS","MF_ATTRIBUTES_MATCH_SMALLER","MF_ATTRIBUTES_MATCH_THEIR_ITEMS","MF_ATTRIBUTES_MATCH_TYPE","MF_ATTRIBUTES_MATCH_TYPE enumeration [Media Foundation]","cfa534c4-88c3-4170-b977-c24ea5593f6c","mf.mf_attributes_match_type","mfobjects/MF_ATTRIBUTES_MATCH_ALL_ITEMS","mfobjects/MF_ATTRIBUTES_MATCH_INTERSECTION","mfobjects/MF_ATTRIBUTES_MATCH_OUR_ITEMS","mfobjects/MF_ATTRIBUTES_MATCH_SMALLER","mfobjects/MF_ATTRIBUTES_MATCH_THEIR_ITEMS","mfobjects/MF_ATTRIBUTES_MATCH_TYPE"]
old-location: mf\mf_attributes_match_type.htm
tech.root: mf
ms.assetid: cfa534c4-88c3-4170-b977-c24ea5593f6c
ms.date: 12/05/2018
ms.keywords: MF_ATTRIBUTES_MATCH_ALL_ITEMS, MF_ATTRIBUTES_MATCH_INTERSECTION, MF_ATTRIBUTES_MATCH_OUR_ITEMS, MF_ATTRIBUTES_MATCH_SMALLER, MF_ATTRIBUTES_MATCH_THEIR_ITEMS, MF_ATTRIBUTES_MATCH_TYPE, MF_ATTRIBUTES_MATCH_TYPE enumeration [Media Foundation], cfa534c4-88c3-4170-b977-c24ea5593f6c, mf.mf_attributes_match_type, mfobjects/MF_ATTRIBUTES_MATCH_ALL_ITEMS, mfobjects/MF_ATTRIBUTES_MATCH_INTERSECTION, mfobjects/MF_ATTRIBUTES_MATCH_OUR_ITEMS, mfobjects/MF_ATTRIBUTES_MATCH_SMALLER, mfobjects/MF_ATTRIBUTES_MATCH_THEIR_ITEMS, mfobjects/MF_ATTRIBUTES_MATCH_TYPE
req.header: mfobjects.h
req.include-header: Mfidl.h
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
req.typenames: MF_ATTRIBUTES_MATCH_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_ATTRIBUTES_MATCH_TYPE
 - mfobjects/_MF_ATTRIBUTES_MATCH_TYPE
 - MF_ATTRIBUTES_MATCH_TYPE
 - mfobjects/MF_ATTRIBUTES_MATCH_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MF_ATTRIBUTES_MATCH_TYPE
---

# MF_ATTRIBUTES_MATCH_TYPE enumeration


## -description

Specifies how to compare the attributes on two objects.

## -enum-fields

### -field MF_ATTRIBUTES_MATCH_OUR_ITEMS:0

Check whether all the attributes in <i>pThis</i> exist in <i>pTheirs</i> and have the same data, where <i>pThis</i> is the object whose <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-compare">Compare</a> method is being called and <i>pTheirs</i> is the object given in the <i>pTheirs</i> parameter.

### -field MF_ATTRIBUTES_MATCH_THEIR_ITEMS:1

Check whether all the attributes in <i>pTheirs</i> exist in <i>pThis</i> and have the same data, where <i>pThis</i> is the object whose <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-compare">Compare</a> method is being called and <i>pTheirs</i> is the object given in the <i>pTheirs</i> parameter.

### -field MF_ATTRIBUTES_MATCH_ALL_ITEMS:2

Check whether both objects have identical attributes with the same data.

### -field MF_ATTRIBUTES_MATCH_INTERSECTION:3

Check whether the attributes that exist in both objects have the same data.

### -field MF_ATTRIBUTES_MATCH_SMALLER:4

Find the object with the fewest number of attributes, and check if those attributes exist in the other object and have the same data.

## -see-also

<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-compare">IMFAttributes::Compare</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
