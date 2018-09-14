---
UID: NE:docobj.OLECMDF
title: OLECMDF
author: windows-sdk-content
description: Specifies the type of support provided by an object for the command specified in an OLECMD structure.
old-location: com\olecmdf.htm
tech.root: com
ms.assetid: feb493da-0db2-4251-ba6f-ded1fbd3e430
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: OLECMDF, OLECMDF enumeration [COM], OLECMDF_DEFHIDEONCTXTMENU, OLECMDF_ENABLED, OLECMDF_INVISIBLE, OLECMDF_LATCHED, OLECMDF_NINCHED, OLECMDF_SUPPORTED, _ole_OLECMDF, com.olecmdf, docobj/OLECMDF, docobj/OLECMDF_DEFHIDEONCTXTMENU, docobj/OLECMDF_ENABLED, docobj/OLECMDF_INVISIBLE, docobj/OLECMDF_LATCHED, docobj/OLECMDF_NINCHED, docobj/OLECMDF_SUPPORTED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: OLECMDF
req.redist: 
---

# OLECMDF enumeration


## -description


Specifies the type of support provided by an object for the command specified in an <a href="https://msdn.microsoft.com/a75ca136-ed6a-43c5-b775-a50535431f1d">OLECMD</a> structure.


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



Values from the <b>OLECMDF</b> enumeration are used to fill the value of the <b>cmdf</b> member of <a href="https://msdn.microsoft.com/a75ca136-ed6a-43c5-b775-a50535431f1d">OLECMD</a> structures passed to <a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>.




## -see-also




<a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>



<a href="https://msdn.microsoft.com/a75ca136-ed6a-43c5-b775-a50535431f1d">OLECMD</a>
 

 

