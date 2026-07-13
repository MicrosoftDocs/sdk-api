---
UID: NS:accctrl._ACTRL_PROPERTY_ENTRYW
title: ACTRL_PROPERTY_ENTRYW (accctrl.h)
description: Contains a list of access-control entries for an object or a specified property on an object. (Unicode)
helpviewer_keywords: ["*PACTRL_PROPERTY_ENTRYW","ACTRL_ACCESS_PROTECTED","ACTRL_PROPERTY_ENTRY","ACTRL_PROPERTY_ENTRY structure [COM]","ACTRL_PROPERTY_ENTRYA","ACTRL_PROPERTY_ENTRYW","PACTRL_PROPERTY_ENTRY","PACTRL_PROPERTY_ENTRY structure pointer [COM]","_ACTRL_PROPERTY_ENTRYA","_ACTRL_PROPERTY_ENTRYW","accctrl/ACTRL_PROPERTY_ENTRY","accctrl/ACTRL_PROPERTY_ENTRYA","accctrl/ACTRL_PROPERTY_ENTRYW","accctrl/PACTRL_PROPERTY_ENTRY","com.actrl_property_entry"]
old-location: com\actrl_property_entry.htm
tech.root: com
ms.assetid: 90b13dd1-0ca6-4674-b9fa-a61aed4637d7
ms.date: 12/05/2018
ms.keywords: '*PACTRL_PROPERTY_ENTRYW, ACTRL_ACCESS_PROTECTED, ACTRL_PROPERTY_ENTRY, ACTRL_PROPERTY_ENTRY structure [COM], ACTRL_PROPERTY_ENTRYA, ACTRL_PROPERTY_ENTRYW, PACTRL_PROPERTY_ENTRY, PACTRL_PROPERTY_ENTRY structure pointer [COM], _ACTRL_PROPERTY_ENTRYA, _ACTRL_PROPERTY_ENTRYW, accctrl/ACTRL_PROPERTY_ENTRY, accctrl/ACTRL_PROPERTY_ENTRYA, accctrl/ACTRL_PROPERTY_ENTRYW, accctrl/PACTRL_PROPERTY_ENTRY, com.actrl_property_entry'
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ACTRL_PROPERTY_ENTRYW (Unicode) and ACTRL_PROPERTY_ENTRYA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACTRL_PROPERTY_ENTRYW, *PACTRL_PROPERTY_ENTRYW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACTRL_PROPERTY_ENTRYW
 - accctrl/_ACTRL_PROPERTY_ENTRYW
 - PACTRL_PROPERTY_ENTRYW
 - accctrl/PACTRL_PROPERTY_ENTRYW
 - ACTRL_PROPERTY_ENTRYW
 - accctrl/ACTRL_PROPERTY_ENTRYW
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
 - ACTRL_PROPERTY_ENTRY
 - ACTRL_PROPERTY_ENTRYA
 - ACTRL_PROPERTY_ENTRYW
---

# ACTRL_PROPERTY_ENTRYW structure


## -description

Contains a list of access-control entries for an object or a specified property on an object.

## -struct-fields

### -field lpProperty

The GUID of a property on an object. Use the <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring">UuidToString</a> function to generate a string representation of a property GUID.

### -field pAccessEntryList

A pointer to an <a href="/windows/desktop/api/accctrl/ns-accctrl-actrl_access_entry_lista">ACTRL_ACCESS_ENTRY_LIST</a> structure that contains a list of access-control entries.

### -field fListFlags

Flags that specify information about the <b>pProperty</b> property. This member can be 0 or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACTRL_ACCESS_PROTECTED_"></a><a id="actrl_access_protected_"></a><dl>
<dt><b>ACTRL_ACCESS_PROTECTED
</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Protects the object or property from inheriting access-control entries.


</td>
</tr>
</table>

## -remarks

To create an <b>ACTRL_PROPERTY_ENTRY</b> structure that grants everyone full access to an object, set the <b>pAccessEntryList</b> member to <b>NULL</b>. 



To create an <b>ACTRL_PROPERTY_ENTRY</b> structure that denies all access to an object, set the <b>pAccessEntryList</b> member to point to an <a href="/windows/desktop/api/accctrl/ns-accctrl-actrl_access_entry_lista">ACTRL_ACCESS_ENTRY_LIST</a> structure whose <b>cEntries</b> member is 0 and <b>pAccessList</b> member is <b>NULL</b>. 





> [!NOTE]
> The accctrl.h header defines ACTRL_PROPERTY_ENTRY as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/accctrl/ns-accctrl-actrl_access_entry_lista">ACTRL_ACCESS_ENTRY_LIST</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring">UuidToString</a>
