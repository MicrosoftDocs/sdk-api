---
UID: NS:oaidl.tagVARDESC
title: VARDESC (oaidl.h)
description: Describes a variable, constant, or data member.
helpviewer_keywords: ["*LPVARDESC","LPVARDESC","LPVARDESC structure pointer [Automation]","VARDESC","VARDESC structure [Automation]","_oa96_VARDESC","automat.vardesc","oaidl/LPVARDESC","oaidl/VARDESC"]
old-location: automat\vardesc.htm
tech.root: automat
ms.assetid: 9584977d-41c4-4f73-8844-2135750ddb80
ms.date: 12/05/2018
ms.keywords: '*LPVARDESC, LPVARDESC, LPVARDESC structure pointer [Automation], VARDESC, VARDESC structure [Automation], _oa96_VARDESC, automat.vardesc, oaidl/LPVARDESC, oaidl/VARDESC'
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: VARDESC, *LPVARDESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVARDESC
 - oaidl/tagVARDESC
 - LPVARDESC
 - oaidl/LPVARDESC
 - VARDESC
 - oaidl/VARDESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - VARDESC
---

# VARDESC structure


## -description

Describes a variable, constant, or data member.

## -struct-fields

### -field memid

The member ID.

### -field lpstrSchema

Reserved.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.oInst

With VAR_PERINSTANCE, the offset of this variable within the instance.

### -field DUMMYUNIONNAME.lpvarValue

With VAR_CONST, the value of the constant.

### -field elemdescVar

The variable type.

### -field wVarFlags

The variable flags. See <a href="/windows/desktop/api/oaidl/ne-oaidl-varflags">VARFLAGS</a>.

### -field varkind

The variable type.