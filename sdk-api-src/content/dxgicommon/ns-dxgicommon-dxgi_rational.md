---
UID: NS:dxgicommon.DXGI_RATIONAL
title: DXGI_RATIONAL
author: windows-sdk-content
description: Represents a rational number.
old-location: direct3ddxgi\dxgi_rational.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_rational.htm
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 5deaf109-e4cc-0f12-82f4-0d4d0b2e387a, DXGI_RATIONAL, DXGI_RATIONAL structure [DXGI], direct3ddxgi.dxgi_rational, dxgicommon/DXGI_RATIONAL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgicommon.h
req.include-header: DXGI.h
req.target-type: Windows
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
 - HeaderDef
api_location:
 - dxgicommon.h
api_name:
 - DXGI_RATIONAL
product: Windows
targetos: Windows
req.typenames: DXGI_RATIONAL
req.redist: 
---

# DXGI_RATIONAL structure


## -description


Represents a rational number.


## -struct-fields




### -field Numerator

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An unsigned integer value representing the top of the rational number.


### -field Denominator

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An unsigned integer value representing the bottom of the rational number.


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/en-us/library/Bb173064(v=VS.85).aspx">DXGI_MODE_DESC</a> structure.

The <b>DXGI_RATIONAL</b> structure operates under the following rules:

<ul>
<li>0/0 is legal and will be interpreted as 0/1.</li>
<li>0/anything is interpreted as zero.</li>
<li>If you are representing a whole number, the denominator should be 1.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

