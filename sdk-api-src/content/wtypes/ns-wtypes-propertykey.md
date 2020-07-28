---
UID: NS:wtypes._tagpropertykey
title: PROPERTYKEY (wtypes.h)
description: Specifies the FMTID/PID identifier that programmatically identifies a property. Replaces SHCOLUMNID.
helpviewer_keywords: ["PROPERTYKEY","PROPERTYKEY structure [Windows Properties]","_shell_PROPERTYKEY","_shell_PROPERTYKEY_cpp","properties.PROPERTYKEY","shell.PROPERTYKEY","wtypes/PROPERTYKEY"]
old-location: properties\PROPERTYKEY.htm
tech.root: properties
ms.assetid: 3f5f31af-f040-443b-9045-9761055381ea
ms.date: 12/05/2018
ms.keywords: PROPERTYKEY, PROPERTYKEY structure [Windows Properties], _shell_PROPERTYKEY, _shell_PROPERTYKEY_cpp, properties.PROPERTYKEY, shell.PROPERTYKEY, wtypes/PROPERTYKEY
f1_keywords:
- wtypes/PROPERTYKEY
dev_langs:
- c++
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wtypes.h
api_name:
- PROPERTYKEY
targetos: Windows
req.typenames: PROPERTYKEY
req.redist: 
ms.custom: 19H1
---

# PROPERTYKEY structure


## -description


Specifies the FMTID/PID identifier that programmatically identifies a property. Replaces <a href="https://docs.microsoft.com/windows/desktop/shell/objects">SHCOLUMNID</a>.


## -struct-fields




### -field fmtid

Type: <b>GUID</b>

A unique GUID for the property.


### -field pid

Type: <b>DWORD</b>

A property identifier (PID). This parameter is not used as in <a href="https://docs.microsoft.com/windows/desktop/shell/objects">SHCOLUMNID</a>. It is recommended that you set this value to PID_FIRST_USABLE. Any value greater than or equal to 2 is acceptable.

<div class="alert"><b>Note</b>  Values of 0 and 1 are reserved and should not be used.</div>
<div> </div>

## -remarks



As of Windows Vista, the <a href="https://docs.microsoft.com/windows/desktop/shell/objects">SHCOLUMNID</a> structure is simply an alias for <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>, as shown in this declaration from Shobjidl.h.

                


```cpp
typedef PROPERTYKEY SHCOLUMNID;
```



<a href="https://docs.microsoft.com/windows/desktop/shell/objects">SHCOLUMNID</a> can be considered a legacy structure with <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> being the new, preferred form. <b>PROPERTYKEY</b> has a broader purpose than <b>SHCOLUMNID</b>, and the new name is more descriptive of its uses.



