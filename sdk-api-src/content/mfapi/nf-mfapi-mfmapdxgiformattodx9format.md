---
UID: NF:mfapi.MFMapDXGIFormatToDX9Format
title: MFMapDXGIFormatToDX9Format function
author: windows-sdk-content
description: Converts a Microsoft DirectX Graphics Infrastructure (DXGI) format identifier to a Microsoft Direct3D 9 format identifier.
old-location: mf\mfmapdxgiformattodx9format.htm
tech.root: medfound
ms.assetid: D3DF4739-31CC-4D0E-9EF2-6FCCAB8969EF
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MFMapDXGIFormatToDX9Format, MFMapDXGIFormatToDX9Format function [Media Foundation], mf.mfmapdxgiformattodx9format, mfapi/MFMapDXGIFormatToDX9Format
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFMapDXGIFormatToDX9Format
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFMapDXGIFormatToDX9Format function


## -description


Converts a Microsoft DirectX Graphics Infrastructure (DXGI) format identifier to a Microsoft Direct3D 9 format identifier.


## -parameters




### -param dx11 [in]

The <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> value to convert.


## -returns



Returns a <a href="https://msdn.microsoft.com/a1ba825b-0574-4657-8a10-447a3caf8149">D3DFORMAT</a> value or FOURCC code.




## -see-also




<a href="https://msdn.microsoft.com/66B6A512-0371-4984-88B3-CB37BE52AEC5">MFMapDX9FormatToDXGIFormat</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

