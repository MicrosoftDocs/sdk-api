---
UID: NS:docobj._tagOLECMDTEXT
title: "_tagOLECMDTEXT"
author: windows-driver-content
description: Specifies a text name or status string for a single command identifier.
old-location: com\olecmdtext.htm
old-project: com
ms.assetid: c9552d2a-fb51-4d9f-acd5-32b3f20a9e1e
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: OLECMDTEXT, OLECMDTEXT structure [COM], _ole_OLECMDTEXT, _tagOLECMDTEXT, com.olecmdtext, docobj/OLECMDTEXT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OLECMDTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	DocObj.h
api_name:
-	OLECMDTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _tagOLECMDTEXT structure


## -description


Specifies a text name or status string for a single command identifier.


## -struct-fields




### -field cmdtextf

A value from the <a href="https://msdn.microsoft.com/8978331a-33b6-4f57-b5a3-aae305c1d872">OLECMDTEXTF</a> enumeration describing whether the <b>rgwz</b> member contains a command name or status text.


### -field cwActual

The number of characters actually written into the <b>rgwz</b> buffer before <a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a> returns.


### -field cwBuf

The number of elements in the <b>rgwz</b> array.


### -field rgwz

A caller-allocated array of wide characters to receive the command name or status text.



## -see-also




<a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>



<a href="https://msdn.microsoft.com/8978331a-33b6-4f57-b5a3-aae305c1d872">OLECMDTEXTF</a>
 

 

