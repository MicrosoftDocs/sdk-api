---
UID: NF:segment.IMSVidClosedCaptioning.put_Enable
title: IMSVidClosedCaptioning::put_Enable
author: windows-sdk-content
description: The put_Enable method enables or disables closed captioning.
old-location: mstv\imsvidclosedcaptioning_put_enable.htm
tech.root: mstv
ms.assetid: 2485b634-24e9-4945-ae46-0ca7fdb9d92b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidClosedCaptioning interface [Microsoft TV Technologies],put_Enable method, IMSVidClosedCaptioning.put_Enable, IMSVidClosedCaptioning::put_Enable, IMSVidClosedCaptioningput_Enable, mstv.imsvidclosedcaptioning_put_enable, put_Enable, put_Enable method [Microsoft TV Technologies], put_Enable method [Microsoft TV Technologies],IMSVidClosedCaptioning interface, segment/IMSVidClosedCaptioning::put_Enable
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidClosedCaptioning.put_Enable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidClosedCaptioning.put_Enable
: 
---

# IMSVidClosedCaptioning::put_Enable


## -description


The <b>put_Enable</b> method enables or disables closed captioning.


## -parameters




### -param On [in]

Specifies whether to enable or disable the closed captioning feature. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Enable closed captioning.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable closed captioning.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/070a208b-cf4c-41e1-9a5f-76cc444285c9">IMSVidClosedCaptioning Interface</a>



<a href="https://msdn.microsoft.com/2bb46aa7-fd94-4afa-9bba-769472e014ff">IMSVidClosedCaptioning::get_Enable</a>
 

 

