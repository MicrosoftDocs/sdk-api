---
UID: NF:d2d1_3helper.InkPoint
title: InkPoint function
author: windows-sdk-content
description: Creates a D2D1_INK_POINT structure.
old-location: direct2d\inkpoint.htm
tech.root: Direct2D
ms.assetid: 6ab8c30d-1ab8-1148-5cce-29797c5f5ad5
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: InkPoint, InkPoint function [Direct2D], d2d1_3helper/InkPoint, direct2d.inkpoint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_3helper.h
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
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - InkPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InkPoint function


## -description


Creates a <a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a> structure.
        


## -parameters




### -param point [ref]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The x and y coordinates of the point.


### -param radius

Type: <b>FLOAT</b>

The radius of this point. Corresponds to the width of the ink stroke at this point in the stroke.


## -returns



Type: <b><a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a></b>

Returns the created <a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a> structure.
          




## -see-also




<a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a>
 

 

