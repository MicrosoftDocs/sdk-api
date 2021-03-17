---
UID: NS:oleidl.tagOLEVERB
title: OLEVERB (oleidl.h)
description: Defines a verb that an object supports. The IOleObject::EnumVerbs method creates an enumerator that can enumerate these structures for an object, and supplies a pointer to the enumerator's IEnumOLEVERB.
helpviewer_keywords: ["*LPOLEVERB","LPOLEVERB","LPOLEVERB structure pointer [COM]","OLEVERB","OLEVERB structure [COM]","_ole_OLEVERB","com.oleverb","oleidl/LPOLEVERB","oleidl/OLEVERB"]
old-location: com\oleverb.htm
tech.root: com
ms.assetid: 657e3cc3-67fb-4458-8dad-f2a31df1b631
ms.date: 12/05/2018
ms.keywords: '*LPOLEVERB, LPOLEVERB, LPOLEVERB structure pointer [COM], OLEVERB, OLEVERB structure [COM], _ole_OLEVERB, com.oleverb, oleidl/LPOLEVERB, oleidl/OLEVERB'
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: OLEVERB, *LPOLEVERB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOLEVERB
 - oleidl/tagOLEVERB
 - LPOLEVERB
 - oleidl/LPOLEVERB
 - OLEVERB
 - oleidl/OLEVERB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleIdl.h
api_name:
 - OLEVERB
---

# OLEVERB structure


## -description

Defines a verb that an object supports. The <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a> method creates an enumerator that can enumerate these structures for an object, and supplies a pointer to the enumerator's <a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a>.

## -struct-fields

### -field lVerb

Integer identifier associated with this verb.

### -field lpszVerbName

Pointer to a string that contains the verb's name.

### -field fuFlags

In Windows, a group of flags taken from the flag constants beginning with MF_ defined in <a href="/windows/desktop/menurc/u">AppendMenu</a>. Containers should use these flags in building an object's verb menu. All Flags defined in <b>AppendMenu</b> are supported except for MF_BITMAP, MF_OWNERDRAW, and MF_POPUP.

### -field grfAttribs

Combination of the verb attributes in the <a href="/windows/desktop/api/oleidl/ne-oleidl-oleverbattrib">OLEVERBATTRIB</a> enumeration.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>