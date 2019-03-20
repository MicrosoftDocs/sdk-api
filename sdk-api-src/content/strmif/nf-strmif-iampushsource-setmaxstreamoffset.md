---
UID: NF:strmif.IAMPushSource.SetMaxStreamOffset
title: IAMPushSource::SetMaxStreamOffset (strmif.h)
author: windows-sdk-content
description: The SetMaxStreamOffset method specifies the stream offset that will be allowed in the filter graph.
old-location: dshow\iampushsource_setmaxstreamoffset.htm
tech.root: DirectShow
ms.assetid: bbe0aa06-f680-4637-beb3-b94139ee0d54
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMPushSource interface [DirectShow],SetMaxStreamOffset method, IAMPushSource.SetMaxStreamOffset, IAMPushSource::SetMaxStreamOffset, IAMPushSourceSetMaxStreamOffset, SetMaxStreamOffset, SetMaxStreamOffset method [DirectShow], SetMaxStreamOffset method [DirectShow],IAMPushSource interface, dshow.iampushsource_setmaxstreamoffset, strmif/IAMPushSource::SetMaxStreamOffset
ms.topic: method
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
 - IAMPushSource.SetMaxStreamOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMPushSource::SetMaxStreamOffset


## -description



The <code>SetMaxStreamOffset</code> method specifies the stream offset that will be allowed in the filter graph.




## -parameters




### -param rtMaxOffset [in]

Reference time specifying the maximum stream offset.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



If this method is called prior to connecting the filter, the filter can allocate an appropriately sized buffer.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5ab294a8-f250-405c-a589-68998bc04cdf">IAMPushSource Interface</a>
 

 

