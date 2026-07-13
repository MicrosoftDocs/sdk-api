---
UID: NF:propkeydef.DEFINE_PROPERTYKEY
title: DEFINE_PROPERTYKEY macro (propkeydef.h)
description: Used to pack a format identifier (FMTID) and property identifier (PID) into a PROPERTYKEY structure that represents a property key.
helpviewer_keywords: ["DEFINE_PROPERTYKEY","DEFINE_PROPERTYKEY macro [Windows Shell]","_shell_DEFINE_PROPERTYKEY","propkeydef/DEFINE_PROPERTYKEY","shell.DEFINE_PROPERTYKEY"]
old-location: shell\DEFINE_PROPERTYKEY.htm
tech.root: shell
ms.assetid: 099F8A20-63E4-4712-97F3-82C61A0C2DE0
ms.date: 07/01/2025
ms.keywords: DEFINE_PROPERTYKEY, DEFINE_PROPERTYKEY macro [Windows Shell], _shell_DEFINE_PROPERTYKEY, propkeydef/DEFINE_PROPERTYKEY, shell.DEFINE_PROPERTYKEY
req.header: propkeydef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DEFINE_PROPERTYKEY
 - propkeydef/DEFINE_PROPERTYKEY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propkeydef.h
api_name:
 - DEFINE_PROPERTYKEY
---

# DEFINE_PROPERTYKEY macro

## -syntax

```cpp
void DEFINE_PROPERTYKEY(
     name,
    DWORD l,
    WORD w1,
    WORD w2,
    BYTE b1,
    BYTE b2,
    BYTE b3,
    BYTE b4,
    BYTE b5,
    BYTE b6,
    BYTE b7,
    BYTE b8,
    DWORD pid
);
```


## -description

Used to pack a format identifier (FMTID) and property identifier (PID) into a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure that represents a property key.

## -parameters

### -param name

The name of a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure that represents a property key.

### -param l

The value of the <b>Data1</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param w1

The value of the <b>Data2</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param w2

The value of the <b>Data3</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param b1

The value of the <b>Data4[0]</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param b2

The value of the <b>Data4[1]</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param b3

The value of the <b>Data4[2]</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param b4

The value of the <b>Data4[3]</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param b5

The value of the <b>Data4[4]</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param b6

The value of the <b>Data4[5]</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param b7

The value of the <b>Data4[6]</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param b8

The value of the <b>Data4[7]</b> member of the <b>fmtid</b> member of the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param pid

A property identifier (PID). It is recommended that you set this value to PID_FIRST_USABLE. Any value greater than or equal to 2 is acceptable.
                    
                        

<div class="alert"><b>Note</b>  Values of 0 and 1 are reserved and should not be used.</div>
<div> </div>

## -remarks

The <b>DEFINE_PROPERTYKEY</b> macro is defined as follows. 
			
                


```
#ifdef INITGUID
#define DEFINE_PROPERTYKEY(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8, pid) \
EXTERN_C const PROPERTYKEY DECLSPEC_SELECTANY name = \
{ { l, w1, w2, { b1, b2,  b3,  b4,  b5,  b6,  b7,  b8 } }, pid }
#else
#define DEFINE_PROPERTYKEY(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8, pid) \ 
EXTERN_C const PROPERTYKEY name
#endif // INITGUID 
```


When using this macro, you have two options:
                
                

<ul>
<li>Include Initguid.h in your project. In this case, the macro declares the property key names and defines the property keys for you. This approach works in most cases, but can cause naming collisions in large, complex projects.</li>
<li>Do not include Initguid.h. Instead, compile your definitions into a static library file that has the .lib file name extension. In this case, the macro declares the property key names for the compiler to use, but you must reference your .lib file in the linker settings for your project. This approach works best in large projects that use multiple modules because it avoids the naming collisions mentioned in option 1.</li>
</ul>
Using the macro without including Initguid.h and without referencing a library file raises the LNK2001 linker error.
