---
UID: NS:naptypes.tagCountedString
title: CountedString (naptypes.h)
description: Defines a null-terminated string with a defined length.
helpviewer_keywords: ["CountedString","CountedString structure [NAP]","StringCorrelationId","nap.countedstring_struct","naptypes/CountedString"]
old-location: nap\countedstring_struct.htm
tech.root: NAP
ms.assetid: 92261dd3-504d-4a4b-b6fa-86f4f97a0df0
ms.date: 12/05/2018
ms.keywords: CountedString, CountedString structure [NAP], StringCorrelationId, nap.countedstring_struct, naptypes/CountedString
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CountedString
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCountedString
 - naptypes/tagCountedString
 - CountedString
 - naptypes/CountedString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - CountedString
---

# CountedString structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>CountedString</b> structure defines a null-terminated string with a defined length.

## -struct-fields

### -field length

The size, in characters, of the string within the range 0 to <a href="/windows/desktop/NAP/nap-type-constants">maxStringLength</a>.

<div class="alert"><b>Note</b>  <b>length</b> does not include the null terminator.</div>
<div> </div>

### -field string

A pointer to a null-terminated wide character string of size <b>length</b> + 1.

## -see-also

<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>