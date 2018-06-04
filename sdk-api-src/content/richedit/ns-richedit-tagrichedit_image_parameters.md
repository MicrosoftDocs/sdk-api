---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagRICHEDIT_IMAGE_PARAMETERS structure


## -description


Defines the attributes of an image to be inserted by the <a href="https://msdn.microsoft.com/147B298B-C4A9-455B-9736-A0B09D72902B">EM_INSERTIMAGE</a> message. 


## -struct-fields




### -field xWidth

The width, in HIMETRIC units (0.01 mm), of the image.


### -field yHeight

 


### -field Ascent

If <i>Type</i> is TA_BASELINE, this parameter is the distance, in HIMETRIC units, that the top of the image extends above the text baseline. If <i>Type</i> is TA_BASELINE and ascent is zero, the bottom of the image is placed at the text baseline.


### -field Type

The vertical alignment of the image. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TA_BASELINE"></a><a id="ta_baseline"></a><dl>
<dt><b>TA_BASELINE</b></dt>
</dl>
</td>
<td width="60%">
Align the image relative to the text baseline. 

</td>
</tr>
<tr>
<td width="40%"><a id="TA_BOTTOM"></a><a id="ta_bottom"></a><dl>
<dt><b>TA_BOTTOM</b></dt>
</dl>
</td>
<td width="60%">
Align the bottom of the image at the bottom of the text line. 

</td>
</tr>
<tr>
<td width="40%"><a id="TA_TOP"></a><a id="ta_top"></a><dl>
<dt><b>TA_TOP</b></dt>
</dl>
</td>
<td width="60%">
Align the top of the image at the top of the text line

</td>
</tr>
</table>
 


### -field pwszAlternateText

The alternate text for the image.




### -field pIStream

The stream that contains the image data.


#### - xHeight

The height, in HIMETRIC units, of the image.


## -see-also




<a href="https://msdn.microsoft.com/147B298B-C4A9-455B-9736-A0B09D72902B">EM_INSERTIMAGE</a>
 

 

