---
UID: NS:wabdefs._ADRENTRY
title: ADRENTRY (wabdefs.h)
description: ADRENTRY (wabdefs.h) - do not use. Describes zero or more properties belonging to one or more recipients.
helpviewer_keywords: ["*LPADRENTRY","ADRENTRY","ADRENTRY structure [Windows Address Book]","Gender","Gender structure [Windows Address Book]","_wab_ADRENTRY","wab._wab_ADRENTRY","wabdefs/ADRENTRY"]
old-location: wab\_wab_ADRENTRY.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\adrentry.htm
ms.date: 08/03/2022
ms.keywords: '*LPADRENTRY, ADRENTRY, ADRENTRY structure [Windows Address Book], Gender, Gender structure [Windows Address Book], _wab_ADRENTRY, wab._wab_ADRENTRY, wabdefs/ADRENTRY'
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
req.typenames: ADRENTRY, *LPADRENTRY
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _ADRENTRY
 - wabdefs/_ADRENTRY
 - LPADRENTRY
 - wabdefs/LPADRENTRY
 - ADRENTRY
 - wabdefs/ADRENTRY
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
 - Gender
---

# ADRENTRY structure


## -description

Do not use. Describes zero or more properties belonging to one or more recipients.

## -struct-fields

### -field ulReserved1

Type: <b>ULONG</b>

### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the count of properties in the property value array to which the <b>rgPropVals</b> member points. The <b>cValues</b> member can be zero.

### -field rgPropVals

Type: <b>LPSPropValue</b>

Pointer to a variable of type <a href="/windows/desktop/api/wabdefs/ns-wabdefs-spropvalue">SPropValue</a> that specifies the property value array describing the properties for the recipient. The <b>rgPropVals</b> member can be <b>NULL</b>.
