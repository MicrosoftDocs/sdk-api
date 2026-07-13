---
UID: NS:accctrl._ACTRL_ACCESS_ENTRY_LISTW
title: ACTRL_ACCESS_ENTRY_LISTW (accctrl.h)
description: Contains a list of access entries. (Unicode)
helpviewer_keywords: ["*PACTRL_ACCESS_ENTRY_LISTW","ACTRL_ACCESS_ENTRY_LIST","ACTRL_ACCESS_ENTRY_LIST structure [COM]","ACTRL_ACCESS_ENTRY_LISTA","ACTRL_ACCESS_ENTRY_LISTW","PACTRL_ACCESS_ENTRY_LIST","PACTRL_ACCESS_ENTRY_LIST structure pointer [COM]","_ACTRL_ACCESS_ENTRY_LISTA","_ACTRL_ACCESS_ENTRY_LISTW","accctrl/ACTRL_ACCESS_ENTRY_LIST","accctrl/ACTRL_ACCESS_ENTRY_LISTA","accctrl/ACTRL_ACCESS_ENTRY_LISTW","accctrl/PACTRL_ACCESS_ENTRY_LIST","com.actrl_access_entry_list"]
old-location: com\actrl_access_entry_list.htm
tech.root: com
ms.assetid: d0e71756-0247-4c6b-b8b5-a343121b7406
ms.date: 12/05/2018
ms.keywords: '*PACTRL_ACCESS_ENTRY_LISTW, ACTRL_ACCESS_ENTRY_LIST, ACTRL_ACCESS_ENTRY_LIST structure [COM], ACTRL_ACCESS_ENTRY_LISTA, ACTRL_ACCESS_ENTRY_LISTW, PACTRL_ACCESS_ENTRY_LIST, PACTRL_ACCESS_ENTRY_LIST structure pointer [COM], _ACTRL_ACCESS_ENTRY_LISTA, _ACTRL_ACCESS_ENTRY_LISTW, accctrl/ACTRL_ACCESS_ENTRY_LIST, accctrl/ACTRL_ACCESS_ENTRY_LISTA, accctrl/ACTRL_ACCESS_ENTRY_LISTW, accctrl/PACTRL_ACCESS_ENTRY_LIST, com.actrl_access_entry_list'
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ACTRL_ACCESS_ENTRY_LISTW (Unicode) and ACTRL_ACCESS_ENTRY_LISTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACTRL_ACCESS_ENTRY_LISTW, *PACTRL_ACCESS_ENTRY_LISTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACTRL_ACCESS_ENTRY_LISTW
 - accctrl/_ACTRL_ACCESS_ENTRY_LISTW
 - PACTRL_ACCESS_ENTRY_LISTW
 - accctrl/PACTRL_ACCESS_ENTRY_LISTW
 - ACTRL_ACCESS_ENTRY_LISTW
 - accctrl/ACTRL_ACCESS_ENTRY_LISTW
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
 - ACTRL_ACCESS_ENTRY_LIST
 - ACTRL_ACCESS_ENTRY_LISTA
 - ACTRL_ACCESS_ENTRY_LISTW
---

# ACTRL_ACCESS_ENTRY_LISTW structure


## -description

Contains a list of access entries.

## -struct-fields

### -field cEntries

The number of entries in the <b>pAccessList</b> array.

### -field pAccessList

A pointer to an array of <a href="/windows/desktop/api/accctrl/ns-accctrl-actrl_access_entrya">ACTRL_ACCESS_ENTRY</a> structures. Each structure specifies access-control information for a specified trustee.

### -field pAccessList.size_is

### -field pAccessList.size_is.cEntries

## -remarks

To create an empty access list, set <b>cEntries</b> to zero and <b>pAccessList</b> to <b>NULL</b>. An empty list does not grant access to any trustee, and thus, denies all access to an object.

To create a null access list, set the <b>pAccessEntryList</b> member of the <a href="/windows/desktop/api/accctrl/ns-accctrl-actrl_property_entrya">ACTRL_PROPERTY_ENTRY</a> structure to <b>NULL</b>. A null access list grants everyone full access to the object.





> [!NOTE]
> The accctrl.h header defines ACTRL_ACCESS_ENTRY_LIST as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/accctrl/ns-accctrl-actrl_property_entrya">ACTRL_PROPERTY_ENTRY</a>
