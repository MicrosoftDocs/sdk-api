---
UID: NS:accctrl._ACTRL_ALISTA
title: ACTRL_ACCESSA (accctrl.h)
description: Contains an array of access-control lists for an object and its properties. (ANSI)
helpviewer_keywords: ["*PACTRL_ACCESSA","*PACTRL_AUDITA","ACTRL_ACCESS","ACTRL_ACCESS structure [COM]","ACTRL_ACCESSA","ACTRL_ACCESSW","ACTRL_AUDIT","ACTRL_AUDITA","PACTRL_ACCESS","PACTRL_ACCESS structure pointer [COM]","PACTRL_ACCESSW_ALLOCATE_ALL_NODES","_ACTRL_ALISTA","_ACTRL_ALISTW","accctrl/ACTRL_ACCESS","accctrl/ACTRL_ACCESSA","accctrl/ACTRL_ACCESSW","accctrl/PACTRL_ACCESS","com.actrl_access"]
old-location: com\actrl_access.htm
tech.root: com
ms.assetid: d7fb10c1-ebb8-44cf-b61c-a70a787b324f
ms.date: 12/05/2018
ms.keywords: '*PACTRL_ACCESSA, *PACTRL_AUDITA, ACTRL_ACCESS, ACTRL_ACCESS structure [COM], ACTRL_ACCESSA, ACTRL_ACCESSW, ACTRL_AUDIT, ACTRL_AUDITA, PACTRL_ACCESS, PACTRL_ACCESS structure pointer [COM], PACTRL_ACCESSW_ALLOCATE_ALL_NODES, _ACTRL_ALISTA, _ACTRL_ALISTW, accctrl/ACTRL_ACCESS, accctrl/ACTRL_ACCESSA, accctrl/ACTRL_ACCESSW, accctrl/PACTRL_ACCESS, com.actrl_access'
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ACTRL_ACCESSW (Unicode) and ACTRL_ACCESSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACTRL_ACCESSA, *PACTRL_ACCESSA, ACTRL_AUDITA, *PACTRL_AUDITA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACTRL_ALISTA
 - accctrl/_ACTRL_ALISTA
 - PACTRL_ACCESSA
 - accctrl/PACTRL_ACCESSA
 - ACTRL_ACCESSA
 - accctrl/ACTRL_ACCESSA
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
 - ACTRL_ACCESS
 - ACTRL_ACCESSA
 - ACTRL_ACCESSW
---

# ACTRL_ACCESSA structure


## -description

Contains an array of access-control lists for an object and its properties.

## -struct-fields

### -field cEntries

The number of entries in the <b>pPropertyAccessList</b> array.

### -field pPropertyAccessList

An array of <a href="/windows/desktop/api/accctrl/ns-accctrl-actrl_property_entrya">ACTRL_PROPERTY_ENTRY</a> structures. Each structure contains a list of access-control entries for an object or a specified property on the object.

### -field pPropertyAccessList.size_is

### -field pPropertyAccessList.size_is.cEntries

## -remarks

Note the following type definition.


``` syntax
typedef PACTRL_ACCESSW PACTRL_ACCESSW_ALLOCATE_ALL_NODES;
```





> [!NOTE]
> The accctrl.h header defines ACTRL_ACCESS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/iaccess/nf-iaccess-iaccesscontrol-grantaccessrights">IAccessControl::GrantAccessRights</a>
