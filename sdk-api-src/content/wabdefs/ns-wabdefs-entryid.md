---
UID: NS:wabdefs.ENTRYID
title: ENTRYID (wabdefs.h)
description: Do not use. Contains the entry identifier information for a MAPI object.
helpviewer_keywords: ["*LPENTRYID","ENTRYID","ENTRYID structure [Windows Address Book]","LPENTRYID","LPENTRYID structure pointer [Windows Address Book]","_wab_ENTRYID","wab._wab_ENTRYID","wabdefs/ENTRYID","wabdefs/LPENTRYID"]
old-location: wab\_wab_ENTRYID.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\entryid.htm
ms.date: 12/05/2018
ms.keywords: '*LPENTRYID, ENTRYID, ENTRYID structure [Windows Address Book], LPENTRYID, LPENTRYID structure pointer [Windows Address Book], _wab_ENTRYID, wab._wab_ENTRYID, wabdefs/ENTRYID, wabdefs/LPENTRYID'
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
req.typenames: ENTRYID, *LPENTRYID
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - LPENTRYID
 - wabdefs/LPENTRYID
 - ENTRYID
 - wabdefs/ENTRYID
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
 - ENTRYID
---

# ENTRYID structure


## -description

Do not use. Contains the entry identifier information for a MAPI object.

## -struct-fields

### -field abFlags

Type: <b>BYTE[4]</b>

Array of variables of type <b>BYTE</b> that specifies the bitmask of flags that provide information describing the object.

### -field ab

Type: <b>BYTE[MAPI_DIM]</b>

Array of variables of type <b>BYTE</b> that specifies the binary data used by service providers. Client applications cannot use this array.

