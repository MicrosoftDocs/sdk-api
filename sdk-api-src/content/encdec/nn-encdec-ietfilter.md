---
UID: NN:encdec.IETFilter
title: IETFilter
author: windows-sdk-content
description: The IETFilter interface is exposed by the Encrypter/Tagger filter. Most applications will not have to use this interface.
old-location: mstv\ietfilter.htm
tech.root: mstv
ms.assetid: 9fce6b33-394c-47d2-9d02-7b0dadaa1736
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IETFilter, IETFilter interface [Microsoft TV Technologies], IETFilter interface [Microsoft TV Technologies],described, IETFilterInterface, encdec/IETFilter, mstv.ietfilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: encdec.h
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
 - EncDec.h
api_name:
 - IETFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IETFilter interface


## -description



The <b>IETFilter</b> interface is exposed by the Encrypter/Tagger filter. Most applications will not have to use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IETFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IETFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IETFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac76a634-af8d-4cf7-aab5-9022ce79ff31">get_EvalRatObjOK</a>
</td>
<td align="left" width="63%">
Queries whether the <b>EvalRat</b> object was created successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2ec57fc-ad5b-4f7b-a6d7-68f5ee0607b6">GetCurrLicenseExpDate</a>
</td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d90d0842-2dd3-4b98-b619-1b71f7870be8">GetCurrRating</a>
</td>
<td align="left" width="63%">
Retrieves the current rating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7982c60b-9be1-49c4-8194-f5e52487275e">GetLastErrorCode</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4579b897-8b68-4b95-8dd4-e5fd94195742">SetRecordingOn</a>
</td>
<td align="left" width="63%">
Signals to the Encrypter/Tagger filter that the Video Control is about to start or stop recording.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IETFilter)</code>.




## -see-also




<a href="https://msdn.microsoft.com/abe939a3-5f43-4fdf-9d4d-34b7be8893eb">TV Ratings Interfaces</a>
 

 

