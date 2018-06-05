---
UID: NS:dwmapi._MilMatrix3x2D
title: "_MilMatrix3x2D"
author: windows-sdk-content
description: Specifies a 3x2 matrix that describes a transform.
old-location: dwm\milmatrix3x2d.htm
old-project: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\structures\milmatrix3x2d.htm
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: MIL_MATRIX3X2D, MilMatrix3x2D, MilMatrix3x2D structure [Desktop Window Manager], _MilMatrix3x2D, _udwm_MilMatrix3x2D, _udwm_milmatrix3x2d_cpp, dwm.milmatrix3x2d, dwmapi/MilMatrix3x2D, winui._udwm_milmatrix3x2d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MilMatrix3x2D
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dwmapi.h
api_name:
-	MilMatrix3x2D
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _MilMatrix3x2D structure


## -description


Specifies a 3x2 matrix that describes a transform. 


## -struct-fields




### -field S_11

The value at the (1,1) position of the matrix (first row, first column).


### -field S_12

The value at the (1,2) position of the matrix (first row, second column).


### -field S_21

The value at the (2,1) position of the matrix (second row, first column).


### -field S_22

The value at the (2,2) position of the matrix (second row, second column).


### -field DX

The value at the (3,1) position of the matrix (third row, first column).


### -field DY

The value at the (3,2) position of the matrix (third row, second column).


## -remarks



In Windows Vista, this structure was named MIL_MATRIX3X2D. It was renamed in Windows 7.



