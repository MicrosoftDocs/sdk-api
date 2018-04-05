---
UID: NS:wtypes._tagpropertykey
title: "_tagpropertykey"
author: windows-driver-content
description: Specifies the FMTID/PID identifier that programmatically identifies a property. Replaces SHCOLUMNID.
old-location: properties\PROPERTYKEY.htm
old-project: properties
ms.assetid: 3f5f31af-f040-443b-9045-9761055381ea
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PROPERTYKEY, PROPERTYKEY structure [Windows Properties], _shell_PROPERTYKEY, _shell_PROPERTYKEY_cpp, _tagpropertykey, properties.PROPERTYKEY, shell.PROPERTYKEY, wtypes/PROPERTYKEY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROPERTYKEY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wtypes.h
api_name:
-	PROPERTYKEY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _tagpropertykey structure


## -description


Specifies the FMTID/PID identifier that programmatically identifies a property. Replaces <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a>.


## -struct-fields




### -field fmtid

Type: <b>GUID</b>

A unique GUID for the property.


### -field pid

Type: <b>DWORD</b>

A property identifier (PID). This parameter is not used as in <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a>. It is recommended that you set this value to PID_FIRST_USABLE. Any value greater than or equal to 2 is acceptable.

<div class="alert"><b>Note</b>  Values of 0 and 1 are reserved and should not be used.</div>
<div> </div>

## -remarks



As of Windows Vista, the <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a> structure is simply an alias for <a href="shell.PROPERTYKEY">PROPERTYKEY</a>, as shown in this declaration from Shobjidl.h.

                

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef PROPERTYKEY SHCOLUMNID;</pre>
</td>
</tr>
</table></span></div>

<a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a> can be considered a legacy structure with <a href="shell.PROPERTYKEY">PROPERTYKEY</a> being the new, preferred form. <b>PROPERTYKEY</b> has a broader purpose than <b>SHCOLUMNID</b>, and the new name is more descriptive of its uses.



