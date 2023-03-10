---
UID: NE:objidl.tagBIND_FLAGS
title: BIND_FLAGS (objidl.h)
description: Controls aspects of moniker binding operations.
helpviewer_keywords: ["BIND_FLAGS","BIND_FLAGS enumeration [COM]","BIND_JUSTTESTEXISTENCE","BIND_MAYBOTHERUSER","_com_BIND_FLAGS","com.bind_flags","objidl/BIND_FLAGS","objidl/BIND_JUSTTESTEXISTENCE","objidl/BIND_MAYBOTHERUSER"]
old-location: com\bind_flags.htm
tech.root: com
ms.assetid: e8884e82-5de2-4a1f-b79c-d431afe9e87e
ms.date: 12/05/2018
ms.keywords: BIND_FLAGS, BIND_FLAGS enumeration [COM], BIND_JUSTTESTEXISTENCE, BIND_MAYBOTHERUSER, _com_BIND_FLAGS, com.bind_flags, objidl/BIND_FLAGS, objidl/BIND_JUSTTESTEXISTENCE, objidl/BIND_MAYBOTHERUSER
req.header: objidl.h
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
req.typenames: BIND_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagBIND_FLAGS
 - objidl/tagBIND_FLAGS
 - BIND_FLAGS
 - objidl/BIND_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - BIND_FLAGS
---

# BIND_FLAGS enumeration


## -description

Controls aspects of moniker binding operations.

## -enum-fields

### -field BIND_MAYBOTHERUSER:1

If this flag is specified, the moniker implementation can interact with the end user. Otherwise, the moniker implementation should not interact with the user in any way, such as by asking for a password for a network volume that needs mounting. If prohibited from interacting with the user when it otherwise would, a moniker implementation can use a different algorithm that does not require user interaction, or it can fail with the error MK_E_MUSTBOTHERUSER.

### -field BIND_JUSTTESTEXISTENCE:2

If this flag is specified, the caller is not interested in having the operation carried out, but only in learning whether the operation could have been carried out had this flag not been specified. For example, this flag lets the caller indicate only an interest in finding out whether an object actually exists by using this flag in a <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> call. Moniker implementations can, however, ignore this possible optimization and carry out the operation in full. Callers must be able to deal with both cases.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-bind_opts">BIND_OPTS</a>



[BIND_OPTS2](/windows/win32/api/objidl/ns-objidl-bind_opts2-r1)



[BIND_OPTS3](/windows/win32/api/objidl/ns-objidl-bind_opts3-r1)
