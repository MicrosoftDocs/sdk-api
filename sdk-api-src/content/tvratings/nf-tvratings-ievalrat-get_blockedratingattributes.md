---
UID: NF:tvratings.IEvalRat.get_BlockedRatingAttributes
title: IEvalRat::get_BlockedRatingAttributes (tvratings.h)
author: windows-sdk-content
description: The get_BlockedRatingAttributes method determines whether content is blocked for a given rating system and rating level.
old-location: mstv\ievalrat_get_blockedratingattributes.htm
tech.root: mstv
ms.assetid: d07b6462-958c-4e97-9be1-41941aa6b747
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEvalRat interface [Microsoft TV Technologies],get_BlockedRatingAttributes method, IEvalRat.get_BlockedRatingAttributes, IEvalRat::get_BlockedRatingAttributes, IEvalRatget_BlockedRatingAttributes, get_BlockedRatingAttributes, get_BlockedRatingAttributes method [Microsoft TV Technologies], get_BlockedRatingAttributes method [Microsoft TV Technologies],IEvalRat interface, mstv.ievalrat_get_blockedratingattributes, tvratings/IEvalRat::get_BlockedRatingAttributes
ms.topic: method
req.header: tvratings.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - Tvratings.h
api_name:
 - IEvalRat.get_BlockedRatingAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEvalRat::get_BlockedRatingAttributes


## -description


The <b>get_BlockedRatingAttributes</b> method determines whether content is blocked for a given rating system and rating level.


## -parameters




### -param enSystem [in]

Specifies the rating system, as an <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration type.


### -param enLevel [in]

Specifies the rating level, as an <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration type. The meaning of this value depends on the rating system.


### -param plbfAttrs [out, retval]

[out, retval] Receives a bitwise combination of flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration. The flags indicate whether the overall rating is blocked, or specific attributes within the rating are blocked.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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



If the <b>BfIsBlocked</b> flag is set, all content with the specified rating level will be blocked. If one of the <b>BfIsAttr_X</b> flags is set, any content with that rating level and attribute will be blocked.




## -see-also




<a href="https://msdn.microsoft.com/b37c7e7d-80fd-4a42-a698-c20ffb2a5052">IEvalRat Interface</a>



<a href="https://msdn.microsoft.com/7c6919f0-1270-4dcd-8180-a9af4763c580">IEvalRat::put_BlockedRatingAttributes</a>
 

 

