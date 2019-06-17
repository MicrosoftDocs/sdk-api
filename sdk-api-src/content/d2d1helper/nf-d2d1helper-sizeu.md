---
UID: NF:d2d1helper.SizeU
title: SizeU function (d2d1helper.h)
author: windows-sdk-content
description: Creates a D2D1_SIZE_U structure that contains the specified width and height.
old-location: direct2d\sizeu.htm
tech.root: Direct2D
ms.assetid: 147670e3-c451-401e-9e79-dacd7c33385d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SizeU, SizeU function [Direct2D], d2d1helper/SizeU, direct2d.sizeu
ms.topic: function
f1_keywords: ["d2d1helper/SizeU"]
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
api_name:
 - SizeU
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SizeU function


## -description


Creates a <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-size-u">D2D1_SIZE_U</a> structure that contains the specified width and height.


## -parameters




### -param width

Type: <b>UINT32</b>

The width of the size. The default value is 0.


### -param height

Type: <b>UINT32</b>

The height of the size. The default value is 0.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-size-u">D2D1_SIZE_U</a></b>

The new size structure.



