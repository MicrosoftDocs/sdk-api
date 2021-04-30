---
UID: NS:wabdefs._SPropTagArray
title: SPropTagArray (wabdefs.h)
description: Do not use. Contains an array of property tags.
helpviewer_keywords: ["*LPSPropTagArray","SPropTagArray","SPropTagArray structure [Windows Address Book]","_wab_SPropTagArray","wab._wab_SPropTagArray","wabdefs/SPropTagArray"]
old-location: wab\_wab_SPropTagArray.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\sproptagarray.htm
ms.date: 12/05/2018
ms.keywords: '*LPSPropTagArray, SPropTagArray, SPropTagArray structure [Windows Address Book], _wab_SPropTagArray, wab._wab_SPropTagArray, wabdefs/SPropTagArray'
req.header: wabdefs.h
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
req.typenames: SPropTagArray, *LPSPropTagArray
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _SPropTagArray
 - wabdefs/_SPropTagArray
 - LPSPropTagArray
 - wabdefs/LPSPropTagArray
 - SPropTagArray
 - wabdefs/SPropTagArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - SPropTagArray
---

# SPropTagArray structure


## -description

Do not use. Contains an array of property tags.

## -struct-fields

### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of property tags in the array indicated by the <b>aulPropTag</b> member.

### -field aulPropTag

Type: <b>ULONG[MAPI_DIM]</b>

Array of variables of type <b>ULONG</b> that specify the property tags.

