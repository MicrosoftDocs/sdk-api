---
UID: NS:oaidl.tagFUNCDESC
title: FUNCDESC (oaidl.h)
description: Describes a function. (FUNCDESC)
helpviewer_keywords: ["*LPFUNCDESC","FUNCDESC","FUNCDESC structure [Automation]","LPFUNCDESC","LPFUNCDESC structure pointer [Automation]","_oa96_FUNCDESC","automat.funcdesc","oaidl/FUNCDESC","oaidl/LPFUNCDESC"]
old-location: automat\funcdesc.htm
tech.root: automat
ms.assetid: 9998e0cb-5aa3-4cd8-86eb-34760eb1164e
ms.date: 12/05/2018
ms.keywords: '*LPFUNCDESC, FUNCDESC, FUNCDESC structure [Automation], LPFUNCDESC, LPFUNCDESC structure pointer [Automation], _oa96_FUNCDESC, automat.funcdesc, oaidl/FUNCDESC, oaidl/LPFUNCDESC'
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
req.typenames: FUNCDESC, *LPFUNCDESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFUNCDESC
 - oaidl/tagFUNCDESC
 - LPFUNCDESC
 - oaidl/LPFUNCDESC
 - FUNCDESC
 - oaidl/FUNCDESC
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
 - FUNCDESC
---

# FUNCDESC structure


## -description

Describes a function.

## -struct-fields

### -field memid

The function member ID.

### -field lprgscode

The status code.

### -field lprgelemdescParam

Description of the element.

### -field funckind

Indicates the type of function (virtual, static, or dispatch-only).

### -field invkind

The invocation type. Indicates whether this is a property function, and if so, which type.

### -field callconv

The calling convention.

### -field cParams

The total number of parameters.

### -field cParamsOpt

The number of optional parameters.

### -field oVft

For FUNC_VIRTUAL, specifies the offset in the VTBL.

### -field cScodes

The number of possible return values.

### -field elemdescFunc

The function return type.

### -field wFuncFlags

The function flags. See <a href="/windows/desktop/api/oaidl/ne-oaidl-funcflags">FUNCFLAGS</a>.

## -remarks

The <b>cParams</b> field specifies the total number of required and optional parameters.



The <b>cParamsOpt</b> field specifies the form of optional parameters accepted by the function, as follows:

<ul>
<li>
A value of 0 specifies that no optional arguments are supported.



</li>
<li>
A value of –1 specifies that the method's last parameter is a pointer to a safe array of variants. Any number of variant arguments greater than <b>cParams</b> –1 must be packaged by the caller into a safe array and passed as the final parameter. This array of optional parameters must be freed by the caller after control is returned from the call.



</li>
<li>
Any other number indicates that the last n parameters of the function are variants and do not need to be specified by the caller explicitly. The parameters left unspecified should be filled in by the compiler or interpreter as variants of type VT_ERROR with the value DISP_E_PARAMNOTFOUND.



</li>
</ul>
