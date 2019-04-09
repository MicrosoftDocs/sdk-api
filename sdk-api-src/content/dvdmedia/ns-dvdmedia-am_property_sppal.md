---
UID: NS:dvdmedia._AM_PROPERTY_SPPAL
title: AM_PROPERTY_SPPAL (dvdmedia.h)
author: windows-sdk-content
description: Specifies the DVD subpicture palette.
old-location: dshow\am_property_sppal.htm
tech.root: DirectShow
ms.assetid: ac368cbe-aaf6-42d5-a8bd-3652800af640
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PAM_PROPERTY_SPPAL, AM_PROPERTY_SPPAL, AM_PROPERTY_SPPAL structure [DirectShow], PAM_PROPERTY_SPPAL, PAM_PROPERTY_SPPAL structure pointer [DirectShow], dshow.am_property_sppal, dvdmedia/AM_PROPERTY_SPPAL, dvdmedia/PAM_PROPERTY_SPPAL"
ms.topic: struct
req.header: dvdmedia.h
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
 - Dvdmedia.h
api_name:
 - AM_PROPERTY_SPPAL
product: Windows
targetos: Windows
req.typenames: AM_PROPERTY_SPPAL, *PAM_PROPERTY_SPPAL
req.redist: 
---

# AM_PROPERTY_SPPAL structure


## -description



Specifies the DVD subpicture palette.




## -struct-fields




### -field sppal

Array of 16 YUV elements that correspond to the 4-bit color numbers requested within the subpicture command stream. The YUV elements are of type <a href="https://msdn.microsoft.com/en-us/library/Dd373469(v=VS.85).aspx">AM_DVD_YUV</a>.


## -remarks



The AM_PROPERTY_DVDSUBPIC_PALETTE property uses this structure.




## -see-also




<a href="https://msdn.microsoft.com/ddbfb65c-7630-4e9f-8013-c5d65c62c628">DVD Subpicture Property Set</a>
 

 

