---
UID: NF:mfapi.MFCalculateImageSize
title: MFCalculateImageSize function (mfapi.h)
description: Retrieves the image size, in bytes, for an uncompressed video format.helpviewer_keywords: ["039ee3cd-2221-4405-ba7f-233a93a0271b","MFCalculateImageSize","MFCalculateImageSize function [Media Foundation]","mf.mfcalculateimagesize","mfapi/MFCalculateImageSize"]
old-location: mf\mfcalculateimagesize.htm
tech.root: medfound
ms.assetid: 039ee3cd-2221-4405-ba7f-233a93a0271b
ms.date: 12/05/2018
ms.keywords: 039ee3cd-2221-4405-ba7f-233a93a0271b, MFCalculateImageSize, MFCalculateImageSize function [Media Foundation], mf.mfcalculateimagesize, mfapi/MFCalculateImageSize
f1_keywords:
- mfapi/MFCalculateImageSize
dev_langs:
- c++
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
- MFCalculateImageSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCalculateImageSize function


## -description



Retrieves the image size, in bytes, for an uncompressed video format.




## -parameters




### -param guidSubtype [in]

Media subtype for the video format. For a list of subtypes, see <a href="https://docs.microsoft.com/windows/desktop/medfound/media-type-guids">Media Type GUIDs</a>.


### -param unWidth [in]

Width of the image, in pixels.


### -param unHeight [in]

Height of the image, in pixels.


### -param pcbImageSize [out]

Receives the size of each frame, in bytes. If the format is compressed or is not recognized, the value is zero.


## -returns



The function returns an HRESULT. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

