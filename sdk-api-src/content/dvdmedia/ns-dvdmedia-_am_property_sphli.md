---
UID: NS:dvdmedia._AM_PROPERTY_SPHLI
title: "_AM_PROPERTY_SPHLI"
author: windows-sdk-content
description: Describes the currently selected button from the DVD highlight information.
old-location: dshow\am_property_sphli.htm
old-project: DirectShow
ms.assetid: fc073d53-bebb-47fc-b60c-7467b4df88c1
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: "*PAM_PROPERTY_SPHLI, AM_PROPERTY_SPHLI, AM_PROPERTY_SPHLI structure [DirectShow], PAM_PROPERTY_SPHLI, PAM_PROPERTY_SPHLI structure pointer [DirectShow], _AM_PROPERTY_SPHLI, dshow.am_property_sphli, dvdmedia/AM_PROPERTY_SPHLI, dvdmedia/PAM_PROPERTY_SPHLI"
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
req.typenames: AM_PROPERTY_SPHLI, *PAM_PROPERTY_SPHLI
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_PROPERTY_SPHLI
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _AM_PROPERTY_SPHLI structure


## -description



Describes the currently selected button from the DVD highlight information.




## -struct-fields




### -field HLISS

Highlight status of current selection.


### -field Reserved

Reserved for internal use. Do not use or set.


### -field StartPTM

Start presentation time divided by 90,000.


### -field EndPTM

End presentation time divided by 90,000.


### -field StartX

Start x-coordinate pixel of the current highlight button.


### -field StartY

Start y-coordinate pixel of the current highlight button.


### -field StopX

Ending x-coordinate pixel of the current highlight button.


### -field StopY

Ending y-coordinate pixel of the current highlight button.


### -field ColCon

Color contrast description of type <a href="https://msdn.microsoft.com/9358d860-6187-48d9-81b6-d5d65d73786d">AM_COLCON</a>.


## -remarks



The <b>AM_PROPERTY_DVDSUBPIC_HLI</b> property uses this structure.




## -see-also




<a href="https://msdn.microsoft.com/ddbfb65c-7630-4e9f-8013-c5d65c62c628">DVD Subpicture Property Set</a>
 

 

