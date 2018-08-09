---
UID: NE:oleidl.tagOLECLOSE
title: tagOLECLOSE
author: windows-sdk-content
description: Indicates whether an object should be saved before closing.
old-location: com\oleclose.htm
old-project: com
ms.assetid: 386f24a4-11d7-4471-960e-1a3ff67ba3c5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OLECLOSE, OLECLOSE enumeration [COM], OLECLOSE_NOSAVE, OLECLOSE_PROMPTSAVE, OLECLOSE_SAVEIFDIRTY, _ole_OLECLOSE, com.oleclose, ole/OLECLOSE, ole/OLECLOSE_NOSAVE, ole/OLECLOSE_PROMPTSAVE, ole/OLECLOSE_SAVEIFDIRTY, tagOLECLOSE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: oleidl.h
req.include-header: OleIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIVIEWPROPSW (Unicode) and OLEUIVIEWPROPSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OLECLOSE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ole.h
api_name:
 - OLECLOSE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagOLECLOSE enumeration


## -description


Indicates whether an object should be saved before closing.


## -enum-fields




### -field OLECLOSE_SAVEIFDIRTY

The object should be saved if it is dirty. 


### -field OLECLOSE_NOSAVE

The object should not be saved, even if it is dirty. This flag is typically used when an object is being deleted.


### -field OLECLOSE_PROMPTSAVE

If the object is dirty, the <a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a> implementation should display a dialog box to let the end user determine whether to save the object. However, if the object is in the running state but its user interface is invisible, the end user should not be prompted, and the close should be handled as if OLECLOSE_SAVEIFDIRTY had been specified.



## -see-also




<a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a>
 

 

