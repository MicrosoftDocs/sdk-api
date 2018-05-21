---
UID: NF:msvidctl.IMSVidCtl.put_MaintainAspectRatio
title: IMSVidCtl::put_MaintainAspectRatio
author: windows-driver-content
description: The put_MaintainAspectRatio method specifies whether the Video Control maintains the aspect ratio of the source video.
old-location: mstv\imsvidctl_put_maintainaspectratio.htm
old-project: mstv
ms.assetid: 7f0943b1-3cb9-46dc-8aaf-be22e2464092
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_MaintainAspectRatio method, IMSVidCtl.put_MaintainAspectRatio, IMSVidCtl::put_MaintainAspectRatio, IMSVidCtlput_MaintainAspectRatio, mstv.imsvidctl_put_maintainaspectratio, msvidctl/IMSVidCtl::put_MaintainAspectRatio, put_MaintainAspectRatio, put_MaintainAspectRatio method [Microsoft TV Technologies], put_MaintainAspectRatio method [Microsoft TV Technologies],IMSVidCtl interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msvidctl.h
api_name:
-	IMSVidCtl.put_MaintainAspectRatio
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidCtl::put_MaintainAspectRatio


## -description


The <b>put_MaintainAspectRatio</b> method specifies whether the Video Control maintains the aspect ratio of the source video.


## -parameters




### -param NewValue [in]

Specifies one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The Video Control will maintain the aspect ratio of the source video.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The Video Control will stretch the video to fill the window. (Default.)</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/eebb75d2-d5ee-49d6-b1bf-03b0040564b7">IMSVidCtl::get_MaintainAspectRatio</a>
 

 

