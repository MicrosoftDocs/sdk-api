---
UID: NE:docobj.OLECMDF
title: OLECMDF (docobj.h)
description: Specifies the type of support provided by an object for the command specified in an OLECMD structure.
old-location: com\olecmdf.htm
tech.root: com
ms.assetid: feb493da-0db2-4251-ba6f-ded1fbd3e430
ms.date: 12/05/2018
ms.keywords: OLECMDF, OLECMDF enumeration [COM], OLECMDF_DEFHIDEONCTXTMENU, OLECMDF_ENABLED, OLECMDF_INVISIBLE, OLECMDF_LATCHED, OLECMDF_NINCHED, OLECMDF_SUPPORTED, _ole_OLECMDF, com.olecmdf, docobj/OLECMDF, docobj/OLECMDF_DEFHIDEONCTXTMENU, docobj/OLECMDF_ENABLED, docobj/OLECMDF_INVISIBLE, docobj/OLECMDF_LATCHED, docobj/OLECMDF_NINCHED, docobj/OLECMDF_SUPPORTED
ms.topic: enum
f1_keywords:
- docobj/OLECMDF
dev_langs:
- c++
req.header: docobj.h
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
- DocObj.h
api_name:
- OLECMDF
targetos: Windows
req.typenames: OLECMDF
req.redist: 
ms.custom: 19H1
---

# OLECMDF enumeration


## -description


Specifies the type of support provided by an object for the command specified in an <a href="https://docs.microsoft.com/windows/desktop/api/docobj/ns-docobj-olecmd">OLECMD</a> structure.


## -enum-fields




### -field OLECMDF_SUPPORTED

The command is supported by this object.


### -field OLECMDF_ENABLED

The command is available and enabled.


### -field OLECMDF_LATCHED

The command is an on-off toggle and is currently on.


### -field OLECMDF_NINCHED

Reserved for future use.



### -field OLECMDF_INVISIBLE

The command is hidden.


### -field OLECMDF_DEFHIDEONCTXTMENU

The command is hidden on the context menu.


## -remarks



Values from the <b>OLECMDF</b> enumeration are used to fill the value of the <b>cmdf</b> member of <a href="https://docs.microsoft.com/windows/desktop/api/docobj/ns-docobj-olecmd">OLECMD</a> structures passed to <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-querystatus">IOleCommandTarget::QueryStatus</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-querystatus">IOleCommandTarget::QueryStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/docobj/ns-docobj-olecmd">OLECMD</a>
 

 

