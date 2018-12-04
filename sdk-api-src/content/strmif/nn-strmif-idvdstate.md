---
UID: NN:strmif.IDvdState
title: IDvdState
author: windows-sdk-content
description: The IDvdState interface caches the current state.The object that implements this interface is called a DVD bookmark. You can use it to save and restore the DVD state, which includes the playback location, the user's parental level, and the DVD region.
old-location: dshow\idvdstate.htm
tech.root: DirectShow
ms.assetid: df30a3b9-7541-42a8-b642-3b6450a0345e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDvdState, IDvdState interface [DirectShow], IDvdState interface [DirectShow],described, IDvdStateInterface, dshow.idvdstate, strmif/IDvdState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdState interface


## -description



The <b>IDvdState</b> interface caches the current state.

The object that implements this interface is called a <i>DVD bookmark</i>. You can use it to save and restore the DVD state, which includes the playback location, the user's parental level, and the DVD region.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdState</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvdState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvdState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a3d8dba-4281-4385-b48f-d9d1b1134676">GetDiscID</a>
</td>
<td align="left" width="63%">
Gets the unique identifier (ID) of the disc from which the bookmark was made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f87c128f-d751-4593-ac26-3249b803bbe4">GetParentalLevel</a>
</td>
<td align="left" width="63%">
Retrieves the user's parental level as saved in the <b>DvdState</b> object.

</td>
</tr>
</table> 


## -remarks



To get the current DVD state information from the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a>, call <a href="https://msdn.microsoft.com/403add2b-3dfd-436d-8184-7a14f30f6ea3">IDvdInfo2::GetState</a>. To restore the state, call <a href="https://msdn.microsoft.com/3941b469-46f3-4499-9062-81a873a36292">IDvdControl2::SetState</a>.

The DVD bookmark object also implements <b>IPersistStream</b> and <b>IPersistMemory</b>. You can use these interfaces to persist the state. You can also create an empty bookmark object by calling <b>CoCreateInstance</b>. The object's CLSID is CLSID_DVDState, defined in uuids.h.

Prior to Windows Vista, a bookmark can be used only on the same computer where it was created. Starting in Windows Vista, the DVD Navigator is able to create bookmarks that can be used other computers. To enable this feature, call <a href="https://msdn.microsoft.com/b3b28da8-b0cb-4d76-8184-93572e4b6d06">IDvdControl2::SetOption</a> with the DVD_EnablePortableBookmarks flag, before calling <a href="https://msdn.microsoft.com/403add2b-3dfd-436d-8184-7a14f30f6ea3">GetState</a> or <a href="https://msdn.microsoft.com/3941b469-46f3-4499-9062-81a873a36292">SetState</a>.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>
 

 

