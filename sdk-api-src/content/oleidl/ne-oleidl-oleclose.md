---
UID: NE:oleidl.tagOLECLOSE
title: OLECLOSE (oleidl.h)
author: windows-sdk-content
description: Indicates whether an object should be saved before closing.
old-location: com\oleclose.htm
tech.root: com
ms.assetid: 386f24a4-11d7-4471-960e-1a3ff67ba3c5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OLECLOSE, OLECLOSE enumeration [COM], OLECLOSE_NOSAVE, OLECLOSE_PROMPTSAVE, OLECLOSE_SAVEIFDIRTY, _ole_OLECLOSE, com.oleclose, oleidl/OLECLOSE, oleidl/OLECLOSE_NOSAVE, oleidl/OLECLOSE_PROMPTSAVE, oleidl/OLECLOSE_SAVEIFDIRTY
ms.topic: enum
f1_keywords: ["oleidl/OLECLOSE"]
req.header: oleidl.h
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
 - OleIdl.h
api_name:
 - OLECLOSE
product: Windows
targetos: Windows
req.typenames: OLECLOSE
req.redist: 
ms.custom: 19H1
---

# OLECLOSE enumeration


## -description


Indicates whether an object should be saved before closing.


## -enum-fields




### -field OLECLOSE_SAVEIFDIRTY

The object should be saved if it is dirty. 


### -field OLECLOSE_NOSAVE

The object should not be saved, even if it is dirty. This flag is typically used when an object is being deleted.


### -field OLECLOSE_PROMPTSAVE

If the object is dirty, the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a> implementation should display a dialog box to let the end user determine whether to save the object. However, if the object is in the running state but its user interface is invisible, the end user should not be prompted, and the close should be handled as if OLECLOSE_SAVEIFDIRTY had been specified.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>
 

 

