---
UID: NF:mfapi.MFCreateMediaBufferFromMediaType
title: MFCreateMediaBufferFromMediaType function
author: windows-sdk-content
description: Allocates a system-memory buffer that is optimal for a specified media type.
old-location: mf\mfcreatemediabufferfrommediatype.htm
tech.root: medfound
ms.assetid: 1EBDB616-6FA9-4E4E-9BC6-CA1E382A08D9
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: MFCreateMediaBufferFromMediaType, MFCreateMediaBufferFromMediaType function [Media Foundation], mf.mfcreatemediabufferfrommediatype, mfapi/MFCreateMediaBufferFromMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - MFCreateMediaBufferFromMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateMediaBufferFromMediaType function


## -description


Allocates a system-memory buffer that is optimal for a specified media type.


## -parameters




### -param pMediaType [in]

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type.


### -param llDuration [in]

The sample duration. This value is required for audio formats.


### -param dwMinLength [in]

The minimum size of the buffer, in bytes. The actual buffer size might be larger. Specify zero to allocate the default buffer size for the media type.


### -param dwMinAlignment [in]

The minimum memory alignment for the buffer. Specify zero to use the default memory alignment.


### -param ppBuffer [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For video formats, if the format is recognized, the function creates a 2-D buffer that implements the <a href="https://msdn.microsoft.com/BFA73B1A-F8A7-4100-9DBD-234CCA06F9F5">IMF2DBuffer2</a> interface. Otherwise it creates a linear buffer. To get the  <b>IMF2DBuffer2</b> interface, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the pointer returned in <i>ppBuffer</i>. If the <b>QueryInterface</b> method fails, use the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface to access the buffer memory.

For audio formats, the function allocates a buffer that is large enough to contain <i>llDuration</i> audio samples, or <i>dwMinLength</i>, whichever is larger.

This function always allocates system memory. For Direct3D surfaces, use the <a href="https://msdn.microsoft.com/5D859F36-A82B-488B-A2F6-C697A1AA86BC">MFCreateDXGISurfaceBuffer</a> or <a href="https://msdn.microsoft.com/d1ee158e-5d70-41a4-b746-2ecaea2db92c">MFCreateDXSurfaceBuffer</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

