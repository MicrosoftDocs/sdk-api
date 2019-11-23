---
UID: NF:propvarutil.IsVariantArray
title: IsVariantArray function (propvarutil.h)

description: Specifies whether a variant is an array.
old-location: properties\IsVariantArray.htm
tech.root: properties
ms.assetid: 3e3a4eb0-c50a-4e4a-b3e3-dc760a519901

ms.date: 12/05/2018
ms.keywords: IsVariantArray, IsVariantArray function [Windows Properties], _shell_IsVariantArray, properties.IsVariantArray, propvarutil/IsVariantArray, shell.IsVariantArray
ms.topic: function
f1_keywords: 
 - "propvarutil/IsVariantArray"
dev_langs:
 - c++
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
 - Propvarutil.h
api_name:
 - IsVariantArray
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IsVariantArray function


## -description


Specifies whether a variant is an array.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to the variant being queried.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if variant is an array.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.



