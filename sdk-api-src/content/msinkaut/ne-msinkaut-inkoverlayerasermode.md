---
UID: NE:msinkaut.InkOverlayEraserMode
title: InkOverlayEraserMode
author: windows-sdk-content
description: Specifies the way in which ink is erased from the InkOverlay object and the InkPicture control.This mode is used when the InkOverlayEditingMode is set to Delete.
old-location: tablet\inkoverlayerasermode.htm
old-project: tablet
ms.assetid: e7400a40-9b82-4750-8e92-a39c6f25b7cd
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: IOERM_PointErase, IOERM_StrokeErase, InkOverlayEraserMode, InkOverlayEraserMode enumeration [Tablet PC], e7400a40-9b82-4750-8e92-a39c6f25b7cd, msinkaut/IOERM_PointErase, msinkaut/IOERM_StrokeErase, msinkaut/InkOverlayEraserMode, tablet.inkoverlayerasermode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InkOverlayEraserMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkOverlayEraserMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# InkOverlayEraserMode enumeration


## -description



Specifies the way in which ink is erased from the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object and the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.

This mode is used when the <a href="https://msdn.microsoft.com/de25636c-b8ca-47e4-ae16-182b98ede8f6">InkOverlayEditingMode</a> is set to Delete.




## -enum-fields




### -field IOERM_StrokeErase

 Ink is erased by stroke.

This is the default value.


### -field IOERM_PointErase

Ink is erased by point.


## -see-also




<a href="https://msdn.microsoft.com/f6471163-8209-4dd0-887c-0edd54ebb50e">EraserMode Property [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/8a880a9a-acd4-4cb1-aea7-4d834ecd9490">EraserWidth Property [InkPicture Control]</a>



<a href="https://msdn.microsoft.com/de25636c-b8ca-47e4-ae16-182b98ede8f6">InkOverlayEditingMode Enumeration</a>
 

 

