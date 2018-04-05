---
UID: NF:d2d1helper.SizeU
title: SizeU function
author: windows-driver-content
description: Creates a D2D1_SIZE_U structure that contains the specified width and height.
old-location: direct2d\sizeu.htm
old-project: Direct2D
ms.assetid: 147670e3-c451-401e-9e79-dacd7c33385d
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: SizeU, SizeU function [Direct2D], d2d1helper/SizeU, direct2d.sizeu
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D2D1_VIGNETTE_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D2d1.dll
api_name:
-	SizeU
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# SizeU function


## -description


Creates a <a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a> structure that contains the specified width and height.


## -parameters




### -param width

Type: <b>UINT32</b>

The width of the size. The default value is 0.


### -param height

Type: <b>UINT32</b>

The height of the size. The default value is 0.


## -returns



Type: <b><a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a></b>

The new size structure.



