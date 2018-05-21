---
UID: NF:propkeydef.DEFINE_PROPERTYKEY
title: DEFINE_PROPERTYKEY macro
author: windows-driver-content
description: Used to pack a format identifier (FMTID) and property identifier (PID) into a PROPERTYKEY structure that represents a property key.
old-location: shell\DEFINE_PROPERTYKEY.htm
old-project: shell
ms.assetid: 099F8A20-63E4-4712-97F3-82C61A0C2DE0
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: DEFINE_PROPERTYKEY, DEFINE_PROPERTYKEY macro [Windows Shell], _shell_DEFINE_PROPERTYKEY, propkeydef/DEFINE_PROPERTYKEY, shell.DEFINE_PROPERTYKEY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.typenames: STATPROPSTG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Propkeydef.h
api_name:
-	DEFINE_PROPERTYKEY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DEFINE_PROPERTYKEY macro


## -description


Used to pack a format identifier (FMTID) and property identifier (PID) into a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure that represents a property key.


## -parameters




### -param name

The name of a <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure that represents a property key.


### -param l

The value of the <b>Data1</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param w1

The value of the <b>Data2</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param w2

The value of the <b>Data3</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param b1

The value of the <b>Data4[0]</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param b2

The value of the <b>Data4[1]</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param b3

The value of the <b>Data4[2]</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param b4

The value of the <b>Data4[3]</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param b5

The value of the <b>Data4[4]</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param b6

The value of the <b>Data4[5]</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param b7

The value of the <b>Data4[6]</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param b8

The value of the <b>Data4[7]</b> member of the <b>fmtid</b> member of the <a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a> structure.


### -param pid

A property identifier (PID). It is recommended that you set this value to PID_FIRST_USABLE. Any value greater than or equal to 2 is acceptable.
                    
                        

<div class="alert"><b>Note</b>  Values of 0 and 1 are reserved and should not be used.</div>
<div> </div>

## -remarks



The <b>DEFINE_PROPERTYKEY</b> macro is defined as follows. 
			
                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#ifdef INITGUID
#define DEFINE_PROPERTYKEY(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8, pid) \
EXTERN_C const PROPERTYKEY DECLSPEC_SELECTANY name = \
{ { l, w1, w2, { b1, b2,  b3,  b4,  b5,  b6,  b7,  b8 } }, pid }
#else
#define DEFINE_PROPERTYKEY(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8, pid) \ 
EXTERN_C const PROPERTYKEY name
#endif // INITGUID </pre>
</td>
</tr>
</table></span></div>
When using this macro, you have two options:
                
                

<ul>
<li>Include Initguid.h in your project. In this case, the macro declares the property key names and defines the property keys for you. This approach works in most cases, but can cause naming collisions in large, complex projects.</li>
<li>Do not include Initguid.h. Instead, compile your definitions into a static library file that has the .lib file name extension. In this case, the macro declares the property key names for the compiler to use, but you must reference your .lib file in the linker settings for your project. This approach works best in large projects that use multiple modules because it avoids the naming collisions mentioned in option 1.</li>
</ul>
Using the macro without including Initguid.h and without referencing a library file raises the LNK2001 linker error.



