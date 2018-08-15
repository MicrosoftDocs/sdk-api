---
UID: NF:dshowasf.IAMWMBufferPass.SetNotify
title: IAMWMBufferPass::SetNotify
author: windows-sdk-content
description: The SetNotify method IAMWMBufferPasssets an application-defined callback on the WM ASF Reader or WM ASF Writer filter.
old-location: dshow\iamwmbufferpass_setnotify.htm
old-project: DirectShow
ms.assetid: 4aa6fc71-39a7-4fa5-bfe3-b5b12dd44a2b
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMWMBufferPass interface [DirectShow],SetNotify method, IAMWMBufferPass.SetNotify, IAMWMBufferPass::SetNotify, IAMWMBufferPassSetNotify, SetNotify, SetNotify method [DirectShow], SetNotify method [DirectShow],IAMWMBufferPass interface, dshow.iamwmbufferpass_setnotify, dshowasf/IAMWMBufferPass::SetNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dshowasf.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IAMWMBufferPass.SetNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAMWMBufferPass::SetNotify


## -description



The <code>SetNotify</code> method <a href="https://msdn.microsoft.com/c13fe4e0-0847-4799-92a6-da36375cfbf4">IAMWMBufferPass</a>sets an application-defined callback on the WM ASF Reader or WM ASF Writer filter.




## -parameters




### -param pCallback [in]

Pointer to the application's <a href="https://msdn.microsoft.com/c3a8e01e-a626-4e47-ad98-e22d1fe88906">IAMWMBufferPassCallback</a> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Call this method before putting the filter graph into the run state.




## -see-also




<a href="https://msdn.microsoft.com/c13fe4e0-0847-4799-92a6-da36375cfbf4">IAMWMBufferPass Interface</a>



<a href="https://msdn.microsoft.com/2fae0504-d1da-413a-80dd-de7818f506ef">Using Windows Media in DirectShow</a>
 

 

