---
UID: NE:objidl._THDTYPE
title: "_THDTYPE"
author: windows-sdk-content
description: Indicates whether a particular thread supports a message loop.
old-location: com\thdtype.htm
old-project: com
ms.assetid: c1f9ab7b-8915-4433-ae9f-57b1aedcad4d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: THDTYPE, THDTYPE enumeration [COM], THDTYPE_BLOCKMESSAGES, THDTYPE_PROCESSMESSAGES, _THDTYPE, _com_THDTYPE, com.thdtype, objidlbase/THDTYPE, objidlbase/THDTYPE_BLOCKMESSAGES, objidlbase/THDTYPE_PROCESSMESSAGES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidl.h
req.include-header: Objidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - THDTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: ADAM
---

# _THDTYPE enumeration


## -description


Indicates whether a particular thread supports a message loop.


## -enum-fields




### -field THDTYPE_BLOCKMESSAGES

The thread does not support a message loop. This behavior is associated with multithreaded apartments.


### -field THDTYPE_PROCESSMESSAGES

The thread supports a message loop. This behavior is associated with single-threaded apartments.


## -see-also




<a href="https://msdn.microsoft.com/93437e45-f1e7-4f1f-bffb-ef234c7f5a6b">IComThreadingInfo::GetCurrentThreadType</a>
 

 

