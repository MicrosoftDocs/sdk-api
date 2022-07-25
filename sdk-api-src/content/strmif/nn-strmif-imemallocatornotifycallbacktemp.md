---
UID: NN:strmif.IMemAllocatorNotifyCallbackTemp
title: IMemAllocatorNotifyCallbackTemp (strmif.h)
description: Enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list.
helpviewer_keywords: ["IMemAllocatorNotifyCallbackTemp","IMemAllocatorNotifyCallbackTemp interface [DirectShow]","IMemAllocatorNotifyCallbackTemp interface [DirectShow]","described","IMemAllocatorNotifyCallbackTempInterface","dshow.imemallocatornotifycallbacktemp","strmif/IMemAllocatorNotifyCallbackTemp"]
old-location: dshow\imemallocatornotifycallbacktemp.htm
tech.root: dshow
ms.assetid: 63097b58-8197-4354-8b92-25baaf265df2
ms.date: 12/05/2018
ms.keywords: IMemAllocatorNotifyCallbackTemp, IMemAllocatorNotifyCallbackTemp interface [DirectShow], IMemAllocatorNotifyCallbackTemp interface [DirectShow],described, IMemAllocatorNotifyCallbackTempInterface, dshow.imemallocatornotifycallbacktemp, strmif/IMemAllocatorNotifyCallbackTemp
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMemAllocatorNotifyCallbackTemp
 - strmif/IMemAllocatorNotifyCallbackTemp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMemAllocatorNotifyCallbackTemp
---

# IMemAllocatorNotifyCallbackTemp interface


## -description

<p class="CCE_Message">[<b>IMemAllocatorNotifyCallbackTemp</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

The <b>IMemAllocatorNotifyCallbackTemp</b> interface enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list. To receive callbacks, the filter must implement this interface. For more information, see <a href="/windows/desktop/api/strmif/nn-strmif-imemallocatorcallbacktemp">IMemAllocatorCallbackTemp Interface</a>.

## -inheritance

The <b>IMemAllocatorNotifyCallbackTemp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMemAllocatorNotifyCallbackTemp</b> also has these types of members:

