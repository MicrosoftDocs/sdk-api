---
UID: NF:oleidl.IOleClientSite.RequestNewObjectLayout
title: IOleClientSite::RequestNewObjectLayout (oleidl.h)
author: windows-sdk-content
description: Asks a container to resize the display site for embedded objects.
old-location: com\ioleclientsite_requestnewobjectlayout.htm
tech.root: com
ms.assetid: 68867ddd-fad0-4eef-8e5c-8198366e8e64
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOleClientSite interface [COM],RequestNewObjectLayout method, IOleClientSite.RequestNewObjectLayout, IOleClientSite::RequestNewObjectLayout, RequestNewObjectLayout, RequestNewObjectLayout method [COM], RequestNewObjectLayout method [COM],IOleClientSite interface, _ole_ioleclientsite_requestnewobjectlayout, com.ioleclientsite_requestnewobjectlayout, oleidl/IOleClientSite::RequestNewObjectLayout
ms.topic: method
f1_keywords: 
 - "oleidl/IOleClientSite.RequestNewObjectLayout"
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - OleIdl.h
api_name:
 - IOleClientSite.RequestNewObjectLayout
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleClientSite::RequestNewObjectLayout


## -description


Asks a container to resize the display site for embedded objects.


## -parameters






## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Client site does not support requests for new layout.

</td>
</tr>
</table>
 




## -remarks



This method can either increase or decrease the space. Currently, there is no standard mechanism by which a container can negotiate how much room an object would like. When such a negotiation is defined, responding to this method will be optional for containers.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>
 

 

