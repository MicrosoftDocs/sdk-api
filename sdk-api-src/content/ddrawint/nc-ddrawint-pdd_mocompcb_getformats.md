---
UID: NC:ddrawint.PDD_MOCOMPCB_GETFORMATS
title: PDD_MOCOMPCB_GETFORMATS (ddrawint.h)
author: windows-sdk-content
description: The DdMoCompGetFormats callback function indicates the uncompressed formats to which the hardware can decode the data.
old-location: display\ddmocompgetformats.htm
tech.root: display
ms.assetid: 9df6473f-32a1-49bd-9ddb-2f2adec3cb45
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DdMoCompGetFormats, DdMoCompGetFormats callback function [Display Devices], PDD_MOCOMPCB_GETFORMATS, PDD_MOCOMPCB_GETFORMATS callback, ddfncs_bc9cd90d-e40c-4ddd-9415-3d02c4620618.xml, ddrawint/DdMoCompGetFormats, display.ddmocompgetformats
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdMoCompGetFormats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDD_MOCOMPCB_GETFORMATS callback function


## -description


The <b>DdMoCompGetFormats</b> callback function indicates the uncompressed formats to which the hardware can decode the data.


## -parameters




### -param Arg1








#### - lpGetFormatData

Points to a <a href="https://msdn.microsoft.com/1effebea-1cdb-46e9-a783-5a68863a2756">DD_GETMOCOMPFORMATSDATA</a> structure that contains the uncompressed format information for the hardware.


## -returns



<b>DdMoCompGetFormats</b> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support motion compensation must implement <b>DdMoCompGetFormats</b>.




## -see-also




<a href="https://msdn.microsoft.com/1effebea-1cdb-46e9-a783-5a68863a2756">DD_GETMOCOMPFORMATSDATA</a>
 

 

