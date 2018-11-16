---
UID: NE:callobj.CALLFRAME_NULL
title: CALLFRAME_NULL
author: windows-sdk-content
description: Determines the parameter type to be freed.
old-location: com\callframe_null.htm
tech.root: com
ms.assetid: 99d83bdc-a33b-4233-84c6-350274f42965
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CALLFRAME_NULL, CALLFRAME_NULL enumeration [COM], CALLFRAME_NULL_ALL, CALLFRAME_NULL_INOUT, CALLFRAME_NULL_NONE, CALLFRAME_NULL_OUT, callobj/CALLFRAME_NULL, callobj/CALLFRAME_NULL_ALL, callobj/CALLFRAME_NULL_INOUT, callobj/CALLFRAME_NULL_NONE, callobj/CALLFRAME_NULL_OUT, com.callframe_null
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: callobj.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CallObj.h
api_name:
 - CALLFRAME_NULL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CALLFRAME_NULL enumeration


## -description


Determines the parameter type to be freed.


## -enum-fields




### -field CALLFRAME_NULL_NONE

No values are freed.


### -field CALLFRAME_NULL_INOUT

The data referenced by [in, out] parameters are freed.


### -field CALLFRAME_NULL_OUT

The data referenced by [out] parameters are freed. 


### -field CALLFRAME_NULL_ALL

All [out] and [in, out] parameters are freed. 


## -see-also




<a href="https://msdn.microsoft.com/97261d93-40cf-4a27-9bee-677600c04699">ICallFrame::Free</a>
 

 

