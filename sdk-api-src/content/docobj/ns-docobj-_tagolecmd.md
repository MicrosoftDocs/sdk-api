---
UID: NS:docobj._tagOLECMD
title: "_tagOLECMD"
author: windows-sdk-content
description: Associates command flags from the OLECMDF enumeration with a command identifier through a call to IOleCommandTarget::QueryStatus.
old-location: com\olecmd.htm
tech.root: com
ms.assetid: a75ca136-ed6a-43c5-b775-a50535431f1d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: OLECMD, OLECMD structure [COM], _ole_OLECMD, _tagOLECMD, com.olecmd, docobj/OLECMD
ms.prod: windows
ms.technology: windows-sdk
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
 - OLECMD
product: Windows
targetos: Windows
req.typenames: OLECMD
req.redist: 
---

# _tagOLECMD structure


## -description


Associates command flags from the <a href="https://msdn.microsoft.com/feb493da-0db2-4251-ba6f-ded1fbd3e430">OLECMDF</a> enumeration with a command identifier through a call to <a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>.




## -struct-fields




### -field cmdID

A command identifier; taken from the <a href="https://msdn.microsoft.com/ae1592b6-2afd-4379-a18e-d46b226bc9e2">OLECMDID</a> enumeration.


### -field cmdf

Flags associated with <b>cmdID</b>; taken from the <a href="https://msdn.microsoft.com/feb493da-0db2-4251-ba6f-ded1fbd3e430">OLECMDF</a> enumeration.



## -see-also




<a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>



<a href="https://msdn.microsoft.com/feb493da-0db2-4251-ba6f-ded1fbd3e430">OLECMDF</a>
 

 

