---
UID: NF:segment.IMSVidFeatures.get_Count
title: IMSVidFeatures::get_Count method
author: windows-driver-content
description: The get_Count method retrieves the number of items in the collection.
old-location: mstv\imsvidfeatures_get_count.htm
old-project: mstv
ms.assetid: 45ad322a-d9ec-446d-8c1e-c955049dd257
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidFeatures, IMSVidFeatures interface [Microsoft TV Technologies], get_Count method, IMSVidFeatures::get_Count, IMSVidFeaturesget_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies], IMSVidFeatures interface, get_Count,IMSVidFeatures.get_Count, mstv.imsvidfeatures_get_count, segment/IMSVidFeatures::get_Count
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidFeatures.get_Count
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidFeatures::get_Count method


## -description


The <b>get_Count</b> method retrieves the number of items in the collection.


## -parameters




### -param lCount






#### - plCount [out]

Pointer to a variable that receives the number of items.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/19790fab-0530-4a17-8a3c-a50576fea9ca">IMSVidFeatures Interface</a>
 

 

