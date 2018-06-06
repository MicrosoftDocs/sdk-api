---
UID: NS:dvdmedia._AM_PROPERTY_SPPAL
title: "_AM_PROPERTY_SPPAL"
author: windows-sdk-content
description: Specifies the DVD subpicture palette.
old-location: dshow\am_property_sppal.htm
old-project: DirectShow
ms.assetid: ac368cbe-aaf6-42d5-a8bd-3652800af640
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PAM_PROPERTY_SPPAL, AM_PROPERTY_SPPAL, AM_PROPERTY_SPPAL structure [DirectShow], PAM_PROPERTY_SPPAL, PAM_PROPERTY_SPPAL structure pointer [DirectShow], _AM_PROPERTY_SPPAL, dshow.am_property_sppal, dvdmedia/AM_PROPERTY_SPPAL, dvdmedia/PAM_PROPERTY_SPPAL"
ms.prod: windows
ms.technology: windows-sdk
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
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AM_PROPERTY_SPPAL, *PAM_PROPERTY_SPPAL
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _AM_PROPERTY_SPPAL structure


## -description



Specifies the DVD subpicture palette.




## -struct-fields




### -field sppal

Array of 16 YUV elements that correspond to the 4-bit color numbers requested within the subpicture command stream. The YUV elements are of type <a href="https://msdn.microsoft.com/fb954bc2-4ef1-4a5f-b795-a3b2a8aae8d4">AM_DVD_YUV</a>.


## -remarks



The AM_PROPERTY_DVDSUBPIC_PALETTE property uses this structure.




## -see-also




<a href="https://msdn.microsoft.com/ddbfb65c-7630-4e9f-8013-c5d65c62c628">DVD Subpicture Property Set</a>
 

 

