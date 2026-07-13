---
UID: NS:accctrl._INHERITED_FROMA
title: INHERITED_FROMA (accctrl.h)
description: Provides information about an object's inherited access control entry (ACE). (ANSI)
helpviewer_keywords: ["*PINHERITED_FROMA","INHERITED_FROM","INHERITED_FROM structure [Security]","INHERITED_FROMA","INHERITED_FROMW","PINHERITED_FROM","PINHERITED_FROM structure pointer [Security]","_INHERITED_FROMA","_INHERITED_FROMW","accctrl/INHERITED_FROM","accctrl/INHERITED_FROMA","accctrl/INHERITED_FROMW","accctrl/PINHERITED_FROM","security.inherited_from"]
old-location: security\inherited_from.htm
tech.root: security
ms.assetid: 6839f67a-6c72-406d-b55e-bc366aaad107
ms.date: 12/05/2018
ms.keywords: '*PINHERITED_FROMA, INHERITED_FROM, INHERITED_FROM structure [Security], INHERITED_FROMA, INHERITED_FROMW, PINHERITED_FROM, PINHERITED_FROM structure pointer [Security], _INHERITED_FROMA, _INHERITED_FROMW, accctrl/INHERITED_FROM, accctrl/INHERITED_FROMA, accctrl/INHERITED_FROMW, accctrl/PINHERITED_FROM, security.inherited_from'
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: INHERITED_FROMW (Unicode) and INHERITED_FROMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: INHERITED_FROMA, *PINHERITED_FROMA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INHERITED_FROMA
 - accctrl/_INHERITED_FROMA
 - PINHERITED_FROMA
 - accctrl/PINHERITED_FROMA
 - INHERITED_FROMA
 - accctrl/INHERITED_FROMA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - INHERITED_FROM
 - INHERITED_FROMA
 - INHERITED_FROMW
---

# INHERITED_FROMA structure


## -description

The <b>INHERITED_FROM</b> structure provides information about an object's inherited <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE).

## -struct-fields

### -field GenerationGap

Number of levels, or generations, between the object and the ancestor. Set this to zero for an explicit ACE. If the ancestor cannot be determined for the inherited ACE, set this member to –1.

### -field AncestorName

Name of the ancestor from which the ACE was inherited. For an explicit ACE, set this to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/aclapi/nf-aclapi-freeinheritedfromarray">FreeInheritedFromArray</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getinheritancesourcea">GetInheritanceSource</a>

## -remarks

> [!NOTE]
> The accctrl.h header defines INHERITED_FROM as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
