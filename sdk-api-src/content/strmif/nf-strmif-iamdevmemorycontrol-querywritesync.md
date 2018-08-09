---
UID: NF:strmif.IAMDevMemoryControl.QueryWriteSync
title: IAMDevMemoryControl::QueryWriteSync
author: windows-sdk-content
description: Note  The IAMDevMemoryControl interface is deprecated. Checks if the memory supported by the allocator requires the use of the IAMDevMemoryControl::WriteSync method.
old-location: dshow\iamdevmemorycontrol_querywritesync.htm
old-project: DirectShow
ms.assetid: ec6dd7e2-b1f2-48fa-bf79-2688e286425e
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMDevMemoryControl interface [DirectShow],QueryWriteSync method, IAMDevMemoryControl.QueryWriteSync, IAMDevMemoryControl::QueryWriteSync, IAMDevMemoryControlQueryWriteSync, QueryWriteSync, QueryWriteSync method [DirectShow], QueryWriteSync method [DirectShow],IAMDevMemoryControl interface, dshow.iamdevmemorycontrol_querywritesync, strmif/IAMDevMemoryControl::QueryWriteSync
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMDevMemoryControl.QueryWriteSync
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMDevMemoryControl::QueryWriteSync


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryControl</b> interface is deprecated.</div>
<div> </div>
Checks if the memory supported by the allocator requires the use of the <a href="https://msdn.microsoft.com/46bf7ab6-cc3c-4846-a8f8-97c62ede4aaf">IAMDevMemoryControl::WriteSync</a> method.




## -parameters






## -returns



Returns S_OK if the method is required, or S_FALSE otherwise.




## -remarks



Not all on-board memory needs to have <a href="https://msdn.microsoft.com/46bf7ab6-cc3c-4846-a8f8-97c62ede4aaf">WriteSync</a> called to synchronize with the completed write. This method is used to check if the call is necessary.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9945bffb-6748-4c7d-ba14-91470cf6c651">IAMDevMemoryControl Interface</a>
 

 

