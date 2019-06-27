---
UID: NF:d2d1.ID2D1StrokeStyle.GetDashStyle
title: ID2D1StrokeStyle::GetDashStyle (d2d1.h)
author: windows-sdk-content
description: Gets a value that describes the stroke's dash pattern.
old-location: direct2d\ID2D1StrokeStyle_GetDashStyle.htm
tech.root: Direct2D
ms.assetid: 15d61f2c-9348-47af-a9cf-4706ab0033b7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDashStyle, GetDashStyle method [Direct2D], GetDashStyle method [Direct2D],ID2D1StrokeStyle interface, ID2D1StrokeStyle interface [Direct2D],GetDashStyle method, ID2D1StrokeStyle.GetDashStyle, ID2D1StrokeStyle::GetDashStyle, d2d1/ID2D1StrokeStyle::GetDashStyle, direct2d.ID2D1StrokeStyle_GetDashStyle
ms.topic: method
f1_keywords: 
 - "d2d1/ID2D1StrokeStyle.GetDashStyle"
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1StrokeStyle.GetDashStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1StrokeStyle::GetDashStyle


## -description


Gets a value that describes the stroke's dash pattern.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style">D2D1_DASH_STYLE</a></b>

A value that describes the predefined dash pattern used, or <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style">D2D1_DASH_STYLE_CUSTOM</a> if a custom dash style is used.




## -remarks



If a custom dash style is specified, the dash pattern is described by the dashes array, which can be retrieved by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1strokestyle-getdashes">GetDashes</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a>
 

 

