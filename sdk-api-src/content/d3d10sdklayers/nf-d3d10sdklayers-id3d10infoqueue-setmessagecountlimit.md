---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.SetMessageCountLimit
title: ID3D10InfoQueue::SetMessageCountLimit (d3d10sdklayers.h)
description: Set the maximum number of messages that can be added to the message queue.helpviewer_keywords: ["27e01700-9801-1813-918b-c6687b02eb6f","ID3D10InfoQueue interface [Direct3D 10]","SetMessageCountLimit method","ID3D10InfoQueue.SetMessageCountLimit","ID3D10InfoQueue::SetMessageCountLimit","SetMessageCountLimit","SetMessageCountLimit method [Direct3D 10]","SetMessageCountLimit method [Direct3D 10]","ID3D10InfoQueue interface","d3d10sdklayers/ID3D10InfoQueue::SetMessageCountLimit","direct3d10.id3d10infoqueue_setmessagecountlimit"]
old-location: direct3d10\id3d10infoqueue_setmessagecountlimit.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_setmessagecountlimit.htm
ms.date: 12/05/2018
ms.keywords: 27e01700-9801-1813-918b-c6687b02eb6f, ID3D10InfoQueue interface [Direct3D 10],SetMessageCountLimit method, ID3D10InfoQueue.SetMessageCountLimit, ID3D10InfoQueue::SetMessageCountLimit, SetMessageCountLimit, SetMessageCountLimit method [Direct3D 10], SetMessageCountLimit method [Direct3D 10],ID3D10InfoQueue interface, d3d10sdklayers/ID3D10InfoQueue::SetMessageCountLimit, direct3d10.id3d10infoqueue_setmessagecountlimit
f1_keywords:
- d3d10sdklayers/ID3D10InfoQueue.SetMessageCountLimit
dev_langs:
- c++
req.header: d3d10sdklayers.h
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
- D3D10SDKLayers.h
api_name:
- ID3D10InfoQueue.SetMessageCountLimit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10InfoQueue::SetMessageCountLimit


## -description


Set the maximum number of messages that can be added to the message queue.


## -parameters




### -param MessageCountLimit [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Maximum number of messages that can be added to the message queue. -1 means no limit.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
 

 

