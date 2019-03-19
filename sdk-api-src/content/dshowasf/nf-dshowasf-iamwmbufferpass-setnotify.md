---
UID: NF:dshowasf.IAMWMBufferPass.SetNotify
title: IAMWMBufferPass::SetNotify (dshowasf.h)
author: windows-sdk-content
description: The SetNotify method is used by applications to provide the WM ASF Writer or WM ASF Reader filter with a pointer to the application's IAMWMBufferPassCallback interface.
old-location: wmformat\iamwmbufferpass_setnotify.htm
tech.root: wmformat
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMWMBufferPass interface [windows Media Format],SetNotify method, IAMWMBufferPass.SetNotify, IAMWMBufferPass::SetNotify, IAMWMBufferPassSetNotify, SetNotify, SetNotify method [windows Media Format], SetNotify method [windows Media Format],IAMWMBufferPass interface, dshowasf/IAMWMBufferPass::SetNotify, wmformat.iamwmbufferpass_setnotify
ms.topic: method
req.header: dshowasf.h
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
 - dshowasf.h
api_name:
 - IAMWMBufferPass.SetNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMWMBufferPass::SetNotify


## -description



The <b>SetNotify</b> method is used by applications to provide the WM ASF Writer or <a href="https://msdn.microsoft.com/3d5ca88a-86bd-4d84-b4f4-782564ced58d">WM ASF Reader</a> filter with a pointer to the application's <a href="https://msdn.microsoft.com/5bf0ae2e-504b-471b-bfc9-aa48f534e03f">IAMWMBufferPassCallback</a> interface.




## -parameters




### -param pCallback [in]

Pointer to the application's <b>IAMWMBufferPassCallback</b> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Call this method before putting the filter graph into the run state.




## -see-also




<a href="https://msdn.microsoft.com/aa7513d4-9341-4ddf-ac82-54eb0c6eb5f4">IAMWMBufferPass Interface</a>
 

 

