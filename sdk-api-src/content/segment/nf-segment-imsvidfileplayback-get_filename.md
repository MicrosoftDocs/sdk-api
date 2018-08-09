---
UID: NF:segment.IMSVidFilePlayback.get_FileName
title: IMSVidFilePlayback::get_FileName
author: windows-sdk-content
description: The get_FileName method retrieves the name of the file to play.
old-location: mstv\imsvidfileplayback_get_filename.htm
old-project: mstv
ms.assetid: c8e01204-fb8e-4ebb-97d9-04dda15c491a
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidFilePlayback interface [Microsoft TV Technologies],get_FileName method, IMSVidFilePlayback.get_FileName, IMSVidFilePlayback::get_FileName, IMSVidFilePlaybackget_FileName, get_FileName, get_FileName method [Microsoft TV Technologies], get_FileName method [Microsoft TV Technologies],IMSVidFilePlayback interface, mstv.imsvidfileplayback_get_filename, segment/IMSVidFilePlayback::get_FileName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidFilePlayback.get_FileName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidFilePlayback::get_FileName


## -description


The <b>get_FileName</b> method retrieves the name of the file to play.


## -parameters




### -param FileName [out]

Pointer to a variable that receives the file name.


## -returns



The method returns an <b>HRESULT</b>. Possible values include the following.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The caller must release the returned string, using the <b>CoTaskMemFree</b> function.




## -see-also




<a href="https://msdn.microsoft.com/d6afaf69-5c1b-4f7f-a3cf-51268d6bc2b5">IMSVidFilePlayback Interface</a>
 

 

