---
UID: NF:segment.IMSVidFeatures.Remove
title: IMSVidFeatures::Remove (segment.h)
description: The Remove method removes an item from the collection.helpviewer_keywords: ["IMSVidFeatures interface [Microsoft TV Technologies]","Remove method","IMSVidFeatures.Remove","IMSVidFeatures::Remove","IMSVidFeaturesRemove","Remove","Remove method [Microsoft TV Technologies]","Remove method [Microsoft TV Technologies]","IMSVidFeatures interface","mstv.imsvidfeatures_remove","segment/IMSVidFeatures::Remove"]
old-location: mstv\imsvidfeatures_remove.htm
tech.root: mstv
ms.assetid: 6a9e35e2-231e-4ad6-ac57-e6258df2777f
ms.date: 12/05/2018
ms.keywords: IMSVidFeatures interface [Microsoft TV Technologies],Remove method, IMSVidFeatures.Remove, IMSVidFeatures::Remove, IMSVidFeaturesRemove, Remove, Remove method [Microsoft TV Technologies], Remove method [Microsoft TV Technologies],IMSVidFeatures interface, mstv.imsvidfeatures_remove, segment/IMSVidFeatures::Remove
f1_keywords:
- segment/IMSVidFeatures.Remove
dev_langs:
- c++
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
- IMSVidFeatures.Remove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidFeatures::Remove


## -description


The <b>Remove</b> method removes an item from the collection.


## -parameters




### -param v [in]

<b>VARIANT</b> that specifies the index of the item to remove.


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
<dt><b>DISP_E_BADINDEX</b></dt>
</dl>
</td>
<td width="60%">
The index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Wrong <b>VARIANT</b> type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The collection is read-only; cannot remove any items.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
</table>
 




## -remarks



The <i>v</i> parameter must be a <b>VARIANT</b> that contains an integer type (VT_I4). The valid range is from 0 to <code>IMSVidFeatures::get_Count</code> - 1.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidfeatures">IMSVidFeatures Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidfeatures-add">IMSVidFeatures::Add</a>
 

 

