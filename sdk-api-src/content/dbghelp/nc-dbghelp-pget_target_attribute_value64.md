---
UID: NC:dbghelp.PGET_TARGET_ATTRIBUTE_VALUE64
title: PGET_TARGET_ATTRIBUTE_VALUE6464 (dbghelp.h)
description: PGET_TARGET_ATTRIBUTE_VALUE64 (dbghelp.h) is an application-defined callback function used with the StackWalk2 function.
helpviewer_keywords: ["GetTargetAttributeValueProc64","GetTargetAttributeValueProc64 callback","GetTargetAttributeValueProc64 callback function","PGET_TARGET_ATTRIBUTE_VALUE64","PGET_TARGET_ATTRIBUTE_VALUE64","dbghelp/GetTargetAttributeValue64"]
tech.root: Debug
ms.assetid: A317127E-8551-4cf4-969C-80E0585F55F0
ms.date: 01/23/2025
ms.keywords: GetTargetAttributeValueProc64, GetTargetAttributeValue64 callback, GetTargetAttributeValueProc64 callback function, PGET_TARGET_ATTRIBUTE_VALUE64, dbghelp/GetTargetAttributeValueProc64
req.header: dbghelp.h
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
req.typenames: 
req.redist: DbgHelp.dll 10.0.22621.4602 or later
ms.custom: 22H2
f1_keywords:
 - PGET_TARGET_ATTRIBUTE_VALUE64
 - dbghelp/PGET_TARGET_ATTRIBUTE_VALUE64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - GetTargetAttributeValueProc64
---

# PGET_TARGET_ATTRIBUTE_VALUE64 callback function

## -description

An application-defined callback function used with the [StackWalk2 function](nf-dbghelp-stackwalk2.md). It provides target attribute values which are required for the stack walk.

The **PGET_TARGET_ATTRIBUTE_VALUE64** type defines a pointer to this callback function. **GetTargetAttributeValueProc64** is a placeholder for the application-defined function name.

## -parameters

### -param hProcess [in]

A handle to the process for which the stack trace is generated.

### -param Attribute [in]

A numeric value indicating what atttribute is being requested.  Currently defined values are:

| Name | Value |
| ---- | ----- |
| TARGET_ATTRIBUTE_PACMASK (0x01) | Indicates that the stack walker is requesting the ARM64 pointer authentication mask for the process whose stack is being walked. |

If this attribute is being requested, the *AttributeData* parameter will indicate the address for which the PAC mask is being fetched.  This allows a differentiation between PAC masks for EL0/1/2 (user mode versus kernel mode, etc...).

If PAC is disabled (or the stack walk is not for an ARM64 platform), the implementation should return FALSE indicating that this attribute cannot be provided.

The special value **TARGET_ATTIBUTE_PACMASK_LIVETARGET** (0xffffffffffffffff) may be returned as an indication that the PAC mask is the same as the process calling StackWalk2.

### -param AttributeData [in]

A data value associated with the *Attribute* parameter.  The meaning of this parameter varies depending on the attribute being requested.

### -param AttributeValue [out]

The implementation of the callback must place the value of the requested attribute here before returning success.

## -returns

The function returns whether or not the attribute value was successfully stored in the *AttributeValue* output parameter.  If the given attribute is not recognized or is irrelevant for the platform in question, the function should return FALSE.

## -remarks

```cpp
typedef
BOOL
(__stdcall *PGET_TARGET_ATTRIBUTE_VALUE64)(
    _In_ HANDLE hProcess,
    _In_ DWORD Attribute,
    _In_ DWORD64 AttributeData,
    _Out_ DWORD64 *AttributeValue
    );
```

## -see-also

- [DbgHelp Functions](/windows/desktop/Debug/dbghelp-functions)
- [StackWalk2 function](nf-dbghelp-stackwalk2.md)
