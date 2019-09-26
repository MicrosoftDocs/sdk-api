---
UID: NF:d3d12video.ID3D12VideoDecodeCommandList.Close
title: ID3D12VideoDecodeCommandList::Close
author: windows-sdk-content
description: Indicates that recording to the command list has finished.
tech.root: mf
ms.assetid: 3fcd7926-a57a-452f-99b0-14360b2d3094
ms.author: windowssdkdev
ms.date: 05/28/2019
ms.topic: method
ms.keywords: ID3D12VideoDecodeCommandList::Close, Close, ID3D12VideoDecodeCommandList.Close, ID3D12VideoDecodeCommandList::Close, ID3D12VideoDecodeCommandList.Close
req.header: d3d12video.h
req.include-header:
req.redist:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll: d3d12.dll
req.irql: 
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDecodeCommandList::Close
product: Windows
targetos: Windows

---

# ID3D12VideoDecodeCommandList::Close


## -description

Indicates that recording to the command list has finished.

## -parameters


## -returns

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the following values:
              

<ul>
<li><b>E_FAIL</b> if the command list has already been closed, or an invalid API was called during command list recording.
              </li>
<li><b>E_OUTOFMEMORY</b> if the operating system ran out of memory during recording.
              </li>
<li><b>E_INVALIDARG</b> if an invalid argument was passed to the command list API during recording.
              </li>
</ul>

See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.

## -remarks

The runtime will validate that the command list has not previously been closed.  If an error was encountered during recording, the error code is returned here.  The runtime won't call the close device driver interface (DDI) in this case.

For an example of creating a command list, see [ID3D12GraphicsCommandList::Close method](https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)

## -see-also