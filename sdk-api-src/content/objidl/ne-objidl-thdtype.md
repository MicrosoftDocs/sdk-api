---
UID: NE:objidl._THDTYPE
title: THDTYPE (objidl.h)
description: Indicates whether a particular thread supports a message loop.
old-location: com\thdtype.htm
tech.root: com
ms.assetid: c1f9ab7b-8915-4433-ae9f-57b1aedcad4d
ms.date: 12/05/2018
ms.keywords: THDTYPE, THDTYPE enumeration [COM], THDTYPE_BLOCKMESSAGES, THDTYPE_PROCESSMESSAGES, _com_THDTYPE, com.thdtype, objidlbase/THDTYPE, objidlbase/THDTYPE_BLOCKMESSAGES, objidlbase/THDTYPE_PROCESSMESSAGES
f1_keywords:
- objidl/THDTYPE
dev_langs:
- c++
req.header: objidl.h
req.include-header: Objidl.h
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
- objidlbase.h
api_name:
- THDTYPE
targetos: Windows
req.typenames: THDTYPE
req.redist: 
ms.custom: 19H1
---

# THDTYPE enumeration


## -description


Indicates whether a particular thread supports a message loop.


## -enum-fields




### -field THDTYPE_BLOCKMESSAGES

The thread does not support a message loop. This behavior is associated with multithreaded apartments.


### -field THDTYPE_PROCESSMESSAGES

The thread supports a message loop. This behavior is associated with single-threaded apartments.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icomthreadinginfo-getcurrentthreadtype">IComThreadingInfo::GetCurrentThreadType</a>
 

 

