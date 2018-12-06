---
UID: NF:atscpsipparser.IAtscContentAdvisoryDescriptor.GetRecordRatingDescriptionText
title: IAtscContentAdvisoryDescriptor::GetRecordRatingDescriptionText
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsccontentadvisorydescriptor_getrecordratingdescriptiontext.htm
tech.root: mstv
ms.assetid: 8a94a7ee-1909-4853-a72b-1174ee3c7803
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordRatingDescriptionText, GetRecordRatingDescriptionText method [Microsoft TV Technologies], GetRecordRatingDescriptionText method [Microsoft TV Technologies],IAtscContentAdvisoryDescriptor interface, IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies],GetRecordRatingDescriptionText method, IAtscContentAdvisoryDescriptor.GetRecordRatingDescriptionText, IAtscContentAdvisoryDescriptor::GetRecordRatingDescriptionText, IAtscContentAdvisoryDescriptorGetRecordRatingDescriptionText, atscpsipparser/IAtscContentAdvisoryDescriptor::GetRecordRatingDescriptionText, mstv.iatsccontentadvisorydescriptor_getrecordratingdescriptiontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IAtscContentAdvisoryDescriptor.GetRecordRatingDescriptionText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAtscContentAdvisoryDescriptor::GetRecordRatingDescriptionText


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordRatingDescriptionText</b> method returns the rating description for a specified rating region.


## -parameters




### -param bIndex [in]

Zero-based index of the rating region. To get the number of rating regions, call <a href="https://msdn.microsoft.com/e9571bdb-5b0b-4798-b4dc-37ccee51a8b3">IAtscContentAdvisoryDescriptor::GetRatingRegionCount</a>.


### -param pbLength [out]

Receives the rating_description_length field.


### -param ppText [out]

Receives a pointer to a buffer that contains the rating_description_text field. The text is formatted as a Multiple String Structure as defined by ATSC PSIP Standard A/65. The caller must free the buffer by calling the <b>CoTaskMemFree</b> function.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>bIndex</i> parameter is out of bounds.

</td>
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
 




## -see-also




<a href="https://msdn.microsoft.com/b7379d66-c57b-45e0-9c63-901bf3637f21">IAtscContentAdvisoryDescriptor Interface</a>
 

 

