---
UID: NE:wtypesbase.tagMSHCTX
title: MSHCTX (wtypesbase.h)
description: Specifies the destination context, which is the process in which the unmarshaling is to be done.
helpviewer_keywords: ["MSHCTX","MSHCTX enumeration [COM]","MSHCTX_CROSSCTX","MSHCTX_DIFFERENTMACHINE","MSHCTX_INPROC","MSHCTX_LOCAL","MSHCTX_NOSHAREDMEM","_com_MSHCTX","com.mshctx","wtypesbase/MSHCTX","wtypesbase/MSHCTX_CROSSCTX","wtypesbase/MSHCTX_DIFFERENTMACHINE","wtypesbase/MSHCTX_INPROC","wtypesbase/MSHCTX_LOCAL","wtypesbase/MSHCTX_NOSHAREDMEM"]
old-location: com\mshctx.htm
tech.root: com
ms.assetid: d7d09ab2-96e7-48da-9292-0e4ca6cebe64
ms.date: 12/05/2018
ms.keywords: MSHCTX, MSHCTX enumeration [COM], MSHCTX_CROSSCTX, MSHCTX_DIFFERENTMACHINE, MSHCTX_INPROC, MSHCTX_LOCAL, MSHCTX_NOSHAREDMEM, _com_MSHCTX, com.mshctx, wtypesbase/MSHCTX, wtypesbase/MSHCTX_CROSSCTX, wtypesbase/MSHCTX_DIFFERENTMACHINE, wtypesbase/MSHCTX_INPROC, wtypesbase/MSHCTX_LOCAL, wtypesbase/MSHCTX_NOSHAREDMEM
req.header: wtypesbase.h
req.include-header: WTypes.h
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
req.typenames: MSHCTX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMSHCTX
 - wtypesbase/tagMSHCTX
 - MSHCTX
 - wtypesbase/MSHCTX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wtypesbase.h
api_name:
 - MSHCTX
---

# MSHCTX enumeration


## -description

Specifies the destination context, which is the process in which the unmarshaling is to be done.

## -enum-fields

### -field MSHCTX_LOCAL:0

The unmarshaling process is local and has shared memory access with the marshaling process.

### -field MSHCTX_NOSHAREDMEM:1

The unmarshaling process does not have shared memory access with the marshaling process.

### -field MSHCTX_DIFFERENTMACHINE:2

The unmarshaling process is on a different computer. The marshaling code cannot assume that a particular piece of application code is installed on that computer.

### -field MSHCTX_INPROC:3

The unmarshaling will be done in another apartment in the same process.

### -field MSHCTX_CROSSCTX:4

Create a new context in the current apartment.

### -field MSHCTX_RESERVED1

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmarshalsizemax">CoGetMarshalSizeMax</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal">CoGetStandardMarshal</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>



<a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istdmarshalinfo">IStdMarshalInfo</a>
