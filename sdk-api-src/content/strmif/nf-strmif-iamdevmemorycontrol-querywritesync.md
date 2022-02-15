---
UID: NF:strmif.IAMDevMemoryControl.QueryWriteSync
title: IAMDevMemoryControl::QueryWriteSync (strmif.h)
description: Note  The IAMDevMemoryControl interface is deprecated. Checks if the memory supported by the allocator requires the use of the IAMDevMemoryControl::WriteSync method.
helpviewer_keywords: ["IAMDevMemoryControl interface [DirectShow]","QueryWriteSync method","IAMDevMemoryControl.QueryWriteSync","IAMDevMemoryControl::QueryWriteSync","IAMDevMemoryControlQueryWriteSync","QueryWriteSync","QueryWriteSync method [DirectShow]","QueryWriteSync method [DirectShow]","IAMDevMemoryControl interface","dshow.iamdevmemorycontrol_querywritesync","strmif/IAMDevMemoryControl::QueryWriteSync"]
old-location: dshow\iamdevmemorycontrol_querywritesync.htm
tech.root: dshow
ms.assetid: ec6dd7e2-b1f2-48fa-bf79-2688e286425e
ms.date: 12/05/2018
ms.keywords: IAMDevMemoryControl interface [DirectShow],QueryWriteSync method, IAMDevMemoryControl.QueryWriteSync, IAMDevMemoryControl::QueryWriteSync, IAMDevMemoryControlQueryWriteSync, QueryWriteSync, QueryWriteSync method [DirectShow], QueryWriteSync method [DirectShow],IAMDevMemoryControl interface, dshow.iamdevmemorycontrol_querywritesync, strmif/IAMDevMemoryControl::QueryWriteSync
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMDevMemoryControl::QueryWriteSync
 - strmif/IAMDevMemoryControl::QueryWriteSync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMDevMemoryControl.QueryWriteSync
---

# IAMDevMemoryControl::QueryWriteSync


## -description

<div class="alert"><b>Note</b>  The <b>IAMDevMemoryControl</b> interface is deprecated.</div>
<div> </div>
Checks if the memory supported by the allocator requires the use of the <a href="/windows/desktop/api/strmif/nf-strmif-iamdevmemorycontrol-writesync">IAMDevMemoryControl::WriteSync</a> method.



## -returns

Returns S_OK if the method is required, or S_FALSE otherwise.

## -remarks

Not all on-board memory needs to have <a href="/windows/desktop/api/strmif/nf-strmif-iamdevmemorycontrol-writesync">WriteSync</a> called to synchronize with the completed write. This method is used to check if the call is necessary.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemorycontrol">IAMDevMemoryControl Interface</a>
