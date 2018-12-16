---
UID: NF:mfapi.MFIsFormatYUV
title: MFIsFormatYUV function
author: windows-sdk-content
description: Queries whether a FOURCC code or D3DFORMAT value is a YUV format.
old-location: mf\mfisformatyuv.htm
tech.root: medfound
ms.assetid: dbf6acd3-79c6-4ec2-a867-f2b2d8b41f53
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFIsFormatYUV, MFIsFormatYUV function [Media Foundation], dbf6acd3-79c6-4ec2-a867-f2b2d8b41f53, mf.mfisformatyuv, mfapi/MFIsFormatYUV
ms.topic: function
req.header: mfapi.h
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
req.lib: Evr.lib
req.dll: Evr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - evr.dll
api_name:
 - MFIsFormatYUV
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFIsFormatYUV function


## -description



Queries whether a FOURCC code or <b>D3DFORMAT</b> value is a YUV format.




## -parameters




### -param Format [in]

FOURCC code or <b>D3DFORMAT</b> value.


## -returns



The function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The value specifies a YUV format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The value does not specify a recognized YUV format.

</td>
</tr>
</table>
 




## -remarks



This function checks whether <i>Format</i> specifies a YUV format. Not every YUV format is recognized by this function. However, if a YUV format is not recognized by this function, it is probably not supported for video rendering or DirectX video acceleration (DXVA).




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

