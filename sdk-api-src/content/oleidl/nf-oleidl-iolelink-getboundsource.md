---
UID: NF:oleidl.IOleLink.GetBoundSource
title: IOleLink::GetBoundSource
author: windows-sdk-content
description: Retrieves a pointer to the link source if the connection is active.
old-location: com\iolelink_getboundsource.htm
old-project: com
ms.assetid: 37d24337-eacc-453a-9a90-043ec9b35e9c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetBoundSource, GetBoundSource method [COM], GetBoundSource method [COM],IOleLink interface, IOleLink interface [COM],GetBoundSource method, IOleLink.GetBoundSource, IOleLink::GetBoundSource, _ole_iolelink_getboundsource, com.iolelink_getboundsource, oleidl/IOleLink::GetBoundSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleLink.GetBoundSource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleLink::GetBoundSource


## -description


Retrieves a pointer to the link source if the connection is active.


## -parameters




### -param ppunk [out]

Address of <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> pointer variable that receives the interface pointer to the link source. When successful, the implementation must call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> on <i>ppunk</i>; it is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>. If an error occurs, the implementation sets <i>ppunk</i> to <b>NULL</b>.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>
 




## -remarks



You typically do not need to call <b>IOleLink::GetBoundSource</b>.




## -see-also




<a href="https://msdn.microsoft.com/4a34a90d-df1b-4bbf-8365-9d741c18ff74">IOleLink</a>
 

 

