---
UID: NF:propkeydef.IsEqualPropertyKey
title: IsEqualPropertyKey macro (propkeydef.h)
description: Compares the members of two PROPERTYKEY structures and returns whether they are equal.
helpviewer_keywords: ["IsEqualPropertyKey","IsEqualPropertyKey macro [Windows Shell]","_shell_IsEqualPropertyKey","propkeydef/IsEqualPropertyKey","shell.IsEqualPropertyKey"]
old-location: shell\IsEqualPropertyKey.htm
tech.root: shell
ms.assetid: 89218de5-95c8-440a-bde1-e4a0bc0d0549
ms.date: 12/05/2018
ms.keywords: IsEqualPropertyKey, IsEqualPropertyKey macro [Windows Shell], _shell_IsEqualPropertyKey, propkeydef/IsEqualPropertyKey, shell.IsEqualPropertyKey
f1_keywords:
- propkeydef/IsEqualPropertyKey
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Propkeydef.h
api_name:
- IsEqualPropertyKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsEqualPropertyKey macro


## -description


Compares the members of two <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structures and returns whether they are equal.


## -parameters




### -param a

The first <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>.


### -param b

The second <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>.


## -remarks



The <b>IsEqualPropertyKey</b> macro is defined as follows. 
			


```
#define IsEqualPropertyKey(a, b)   (((a).pid == (b).pid) && IsEqualIID((a).fmtid, (b).fmtid) )
```




