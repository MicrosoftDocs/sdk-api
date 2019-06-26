---
UID: NS:vptype._AMVPDIMINFO
title: AMVPDIMINFO (vptype.h)
author: windows-sdk-content
description: The AMVPDIMINFO structure specifies the dimensional characteristics of a video port (VP) input stream.
old-location: dshow\amvpdiminfo.htm
tech.root: DirectShow
ms.assetid: e39cbb85-33f0-4810-aa32-cc96676da123
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPAMVPDIMINFO, AMVPDIMINFO, AMVPDIMINFO structure [DirectShow], AMVPDIMINFOStructure, LPAMVPDIMINFO, LPAMVPDIMINFO structure pointer [DirectShow], dshow.amvpdiminfo, vptype/AMVPDIMINFO, vptype/LPAMVPDIMINFO"
ms.topic: struct
f1_keywords: 
 - "vptype/AMVPDIMINFO"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - vptype.h
api_name:
 - AMVPDIMINFO
product: Windows
targetos: Windows
req.typenames: AMVPDIMINFO, *LPAMVPDIMINFO
req.redist: 
ms.custom: 19H1
---

# AMVPDIMINFO structure


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

