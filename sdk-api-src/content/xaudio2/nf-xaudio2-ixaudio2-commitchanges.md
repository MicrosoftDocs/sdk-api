---
UID: NF:xaudio2.IXAudio2.CommitChanges
title: IXAudio2::CommitChanges (xaudio2.h)
description: Atomically applies a set of operations that are tagged with a given identifier.
helpviewer_keywords: ["CommitChanges","CommitChanges method [XAudio2 Audio Mixing APIs]","CommitChanges method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","IXAudio2 interface [XAudio2 Audio Mixing APIs]","CommitChanges method","IXAudio2.CommitChanges","IXAudio2::CommitChanges","xaudio2.ixaudio2_interface_commitchanges","xaudio2/IXAudio2::CommitChanges"]
old-location: xaudio2\ixaudio2_interface_commitchanges.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.CommitChanges(UINT32)
ms.date: 12/05/2018
ms.keywords: CommitChanges, CommitChanges method [XAudio2 Audio Mixing APIs], CommitChanges method [XAudio2 Audio Mixing APIs],IXAudio2 interface, IXAudio2 interface [XAudio2 Audio Mixing APIs],CommitChanges method, IXAudio2.CommitChanges, IXAudio2::CommitChanges, xaudio2.ixaudio2_interface_commitchanges, xaudio2/IXAudio2::CommitChanges
req.header: xaudio2.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2::CommitChanges
 - xaudio2/IXAudio2::CommitChanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2.CommitChanges
---

# IXAudio2::CommitChanges


## -description

Atomically applies a set of operations that are tagged with a given identifier.

## -parameters

### -param OperationSet [in]

Identifier of the set of operations to be applied. To commit all pending operations, pass <b>XAUDIO2_COMMIT_ALL</b>.

## -returns

Returns S_OK if successful; returns an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

<b>CommitChanges</b> does nothing if no operations are tagged with the given identifier.



See the <a href="/windows/desktop/xaudio2/xaudio2-operation-sets">XAudio2 Operation Sets</a> overview about working with <b>CommitChanges</b> and XAudio2 interface methods that may be deferred.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>