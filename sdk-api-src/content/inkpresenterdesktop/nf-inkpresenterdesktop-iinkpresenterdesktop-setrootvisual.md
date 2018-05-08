---
UID: NF:inkpresenterdesktop.IInkPresenterDesktop.SetRootVisual
title: IInkPresenterDesktop::SetRootVisual
author: windows-driver-content
description: Sets the connection to the app's DirectComposition visual tree.
old-location: input_ink\iinkpresenterdesktop_setrootvisual.htm
old-project: input_ink
ms.assetid: 27b08f20-d43b-452c-809d-837664eb42d0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IInkPresenterDesktop interface,SetRootVisual method, IInkPresenterDesktop.SetRootVisual, IInkPresenterDesktop::SetRootVisual, InkPresenterDesktop.iinkpresenterdesktop_setrootvisual, SetRootVisual, SetRootVisual method, SetRootVisual method,IInkPresenterDesktop interface, inkpresenterdesktop/IInkPresenterDesktop::SetRootVisual, input_ink.iinkpresenterdesktop_setrootvisual
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: inkpresenterdesktop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InkPresenterDesktop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkPresenterDesktop.h
api_name:
-	IInkPresenterDesktop.SetRootVisual
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkPresenterDesktop::SetRootVisual


## -description


Sets the connection to the app's  <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> visual tree.


## -parameters




### -param rootVisual [in]

The app's  <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> visual tree. 


### -param device [in]

NULL for default ink rendering, or an <a href="https://msdn.microsoft.com/5da076dc-360d-0b28-f131-8669d1a91dd6">IDCompositionDevice3</a> object used to commit all pending DirectComposition commands for custom drying of ink input to the app's  <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> visual tree.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=620314">Complex ink sample</a>



<a href="https://msdn.microsoft.com/6d175981-6379-4a61-84b0-8b08274bc3a3">IInkPresenterDesktop</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620308">Ink sample</a>



<a href="https://msdn.microsoft.com/3DA4F2D2-5405-42A1-9ED9-3A87BCD84C43">Pen and stylus interactions</a>



<b>Samples</b>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620312">Simple ink sample</a>
 

 

