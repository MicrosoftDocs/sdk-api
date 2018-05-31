---
UID: NS:vptype._AMVPDIMINFO
title: "_AMVPDIMINFO"
author: windows-sdk-content
description: The AMVPDIMINFO structure specifies the dimensional characteristics of a video port (VP) input stream.
old-location: dshow\amvpdiminfo.htm
old-project: DirectShow
ms.assetid: e39cbb85-33f0-4810-aa32-cc96676da123
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*LPAMVPDIMINFO, AMVPDIMINFO, AMVPDIMINFO structure [DirectShow], AMVPDIMINFOStructure, LPAMVPDIMINFO, LPAMVPDIMINFO structure pointer [DirectShow], _AMVPDIMINFO, dshow.amvpdiminfo, vptype/AMVPDIMINFO, vptype/LPAMVPDIMINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vptype.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AMVPDIMINFO, *LPAMVPDIMINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	vptype.h
api_name:
-	AMVPDIMINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _AMVPDIMINFO structure


## -description



The <b>AMVPDIMINFO</b> structure specifies the dimensional characteristics of a video port (VP) input stream.




## -struct-fields




### -field dwFieldWidth

Field width of the data.


### -field dwFieldHeight

Field height of the data.


### -field dwVBIWidth

Width of the VBI data.


### -field dwVBIHeight

Height of the VBI data.


### -field rcValidRegion

Valid rectangle, used for cropping.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

