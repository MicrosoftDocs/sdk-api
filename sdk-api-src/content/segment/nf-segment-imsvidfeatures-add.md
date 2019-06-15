---
UID: NF:segment.IMSVidFeatures.Add
title: IMSVidFeatures::Add (segment.h)
author: windows-sdk-content
description: The Add method adds a feature to the collection.
old-location: mstv\imsvidfeatures_add.htm
tech.root: mstv
ms.assetid: 1bdb5e4a-4dd7-49dc-bb9c-b6a9e435219b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Add, Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies],IMSVidFeatures interface, IMSVidFeatures interface [Microsoft TV Technologies],Add method, IMSVidFeatures.Add, IMSVidFeatures::Add, IMSVidFeaturesAdd, mstv.imsvidfeatures_add, segment/IMSVidFeatures::Add
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
 - IMSVidFeatures.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidFeatures::Add


## -description


The <b>Add</b> method adds a feature to the collection.


## -parameters




### -param pDB [in]

Specifies a pointer to the feature's <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidfeature">IMSVidFeature</a> interface.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The collection is read-only; cannot add any items.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidfeatures">IMSVidFeatures Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidfeatures-remove">IMSVidFeatures::Remove</a>
 

 

