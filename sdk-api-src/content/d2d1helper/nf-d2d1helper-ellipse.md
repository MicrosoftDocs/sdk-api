---
UID: NF:d2d1helper.Ellipse
title: Ellipse function
author: windows-sdk-content
description: Creates a D2D1_ELLIPSE structure.
old-location: direct2d\ellipse.htm
tech.root: direct2d
ms.assetid: 49d1b737-acf3-4dd7-81ce-c78ac0558a87
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: Ellipse, Ellipse function [Direct2D], d2d1helper/Ellipse, direct2d.ellipse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1helper.h
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - Ellipse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Ellipse function


## -description


Creates a <a href="https://msdn.microsoft.com/6fed6c49-ba83-4c2b-af8a-04156ee317f0">D2D1_ELLIPSE</a> structure.


## -parameters




### -param center [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The center point of the ellipse.


### -param radiusX

Type: <b>FLOAT</b>

The x-radius of the ellipse.


### -param radiusY

Type: <b>FLOAT</b>

The y-radius of the ellipse.


## -returns



Type: <b><a href="https://msdn.microsoft.com/6fed6c49-ba83-4c2b-af8a-04156ee317f0">D2D1_ELLIPSE</a></b>

The new ellipse.



