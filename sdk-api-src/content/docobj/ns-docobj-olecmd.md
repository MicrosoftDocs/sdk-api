---
UID: NS:docobj._tagOLECMD
title: OLECMD (docobj.h)
description: Associates command flags from the OLECMDF enumeration with a command identifier through a call to IOleCommandTarget::QueryStatus.
helpviewer_keywords: ["OLECMD","OLECMD structure [COM]","_ole_OLECMD","com.olecmd","docobj/OLECMD"]
old-location: com\olecmd.htm
tech.root: com
ms.assetid: a75ca136-ed6a-43c5-b775-a50535431f1d
ms.date: 12/05/2018
ms.keywords: OLECMD, OLECMD structure [COM], _ole_OLECMD, com.olecmd, docobj/OLECMD
req.header: docobj.h
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
req.typenames: OLECMD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagOLECMD
 - docobj/_tagOLECMD
 - OLECMD
 - docobj/OLECMD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DocObj.h
api_name:
 - OLECMD
---

# OLECMD structure


## -description

Associates command flags from the <a href="/windows/desktop/api/docobj/ne-docobj-olecmdf">OLECMDF</a> enumeration with a command identifier through a call to <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-querystatus">IOleCommandTarget::QueryStatus</a>.

## -struct-fields

### -field cmdID

A command identifier; taken from the <a href="/windows/desktop/api/docobj/ne-docobj-olecmdid">OLECMDID</a> enumeration.

### -field cmdf

Flags associated with <b>cmdID</b>; taken from the <a href="/windows/desktop/api/docobj/ne-docobj-olecmdf">OLECMDF</a> enumeration.

## -see-also

<a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-querystatus">IOleCommandTarget::QueryStatus</a>



<a href="/windows/desktop/api/docobj/ne-docobj-olecmdf">OLECMDF</a>