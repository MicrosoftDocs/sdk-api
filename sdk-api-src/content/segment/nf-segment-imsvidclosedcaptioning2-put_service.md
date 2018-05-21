---
UID: NF:segment.IMSVidClosedCaptioning2.put_Service
title: IMSVidClosedCaptioning2::put_Service
author: windows-driver-content
description: The get_Service method sets the closed captioning service.
old-location: mstv\imsvidclosedcaptioning2_put_service.htm
old-project: mstv
ms.assetid: f638a7c3-bd0a-465d-b104-ea0066aec6d6
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IMSVidClosedCaptioning2 interface [Microsoft TV Technologies],put_Service method, IMSVidClosedCaptioning2.put_Service, IMSVidClosedCaptioning2::put_Service, IMSVidClosedCaptioning2put_Service, mstv.imsvidclosedcaptioning2_put_service, put_Service, put_Service method [Microsoft TV Technologies], put_Service method [Microsoft TV Technologies],IMSVidClosedCaptioning2 interface, segment/IMSVidClosedCaptioning2::put_Service
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidClosedCaptioning2.put_Service
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidClosedCaptioning2::put_Service


## -description


The <b>get_Service</b> method sets the closed captioning service.


## -parameters




### -param On






#### - Service [in]

Specifies the closed captioning service, as a member of the <a href="https://msdn.microsoft.com/19e6a389-7f5b-40b9-a7e6-e90060e6d7d5">MSVidCCService</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/37fe213a-7778-4448-937d-30ad1015d56c">IMSVidClosedCaptioning2 Interface</a>
 

 

