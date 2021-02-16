---
UID: NS:wabdefs._SBinaryArray
title: SBinaryArray (wabdefs.h)
description: Do not use. An array of entry identifiers representing MAPI objects. Uses the same implementation as SBinaryArray.
helpviewer_keywords: ["*LPENTRYLIST","ENTRYLIST","ENTRYLIST structure [Windows Address Book]","LPENTRYLIST","LPENTRYLIST structure pointer [Windows Address Book]","SBinaryArray","_wab_ENTRYLIST","wab._wab_ENTRYLIST","wabdefs/ENTRYLIST","wabdefs/LPENTRYLIST"]
old-location: wab\_wab_ENTRYLIST.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\entrylist.htm
ms.date: 12/05/2018
ms.keywords: '*LPENTRYLIST, ENTRYLIST, ENTRYLIST structure [Windows Address Book], LPENTRYLIST, LPENTRYLIST structure pointer [Windows Address Book], SBinaryArray, _wab_ENTRYLIST, wab._wab_ENTRYLIST, wabdefs/ENTRYLIST, wabdefs/LPENTRYLIST'
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
req.typenames: SBinaryArray
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - _SBinaryArray
 - wabdefs/_SBinaryArray
 - SBinaryArray
 - wabdefs/SBinaryArray
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
 - ENTRYLIST
---

# SBinaryArray structure


## -description

Do not use. An array of entry identifiers representing MAPI objects. Uses the same implementation as <a href="/previous-versions/office/developer/office-2007/cc815398(v=office.12)">SBinaryArray</a>.

## -struct-fields

### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of entry identifiers.

### -field lpbin

Type: <b><a href="/previous-versions/office/developer/office-2007/cc815817(v=office.12)">SBinary</a>*</b>

Array of variables of type <a href="/previous-versions/office/developer/office-2007/cc815817(v=office.12)">SBinary</a> that specify the entry identifiers.