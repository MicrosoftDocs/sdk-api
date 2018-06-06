---
UID: NF:msctf.ITfContextOwnerCompositionSink.OnUpdateComposition
title: ITfContextOwnerCompositionSink::OnUpdateComposition
author: windows-sdk-content
description: ITfContextOwnerCompositionSink::OnUpdateComposition method
old-location: tsf\itfcontextownercompositionsink_onupdatecomposition.htm
old-project: TSF
ms.assetid: 18c13a32-918b-4178-a72d-0f7d10c2a68d
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfContextOwnerCompositionSink interface [Text Services Framework],OnUpdateComposition method, ITfContextOwnerCompositionSink.OnUpdateComposition, ITfContextOwnerCompositionSink::OnUpdateComposition, OnUpdateComposition, OnUpdateComposition method [Text Services Framework], OnUpdateComposition method [Text Services Framework],ITfContextOwnerCompositionSink interface, _tsf_itfcontextownercompositionsink_onupdatecomposition_ref, msctf/ITfContextOwnerCompositionSink::OnUpdateComposition, tsf.itfcontextownercompositionsink_onupdatecomposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwnerCompositionSink.OnUpdateComposition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msimtf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContextOwnerCompositionSink::OnUpdateComposition


## -description




## -parameters




### -param pComposition [in]

Pointer to an <a href="https://msdn.microsoft.com/1c8aac3e-384e-402e-aae8-11e240083603">ITfCompositionView</a> object that represents the composition updated.


### -param pRangeNew [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that contains the range of text the composition will cover after the composition is updated.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To determine what has changed within the composition, compare <i>pRangeNew</i> with the range returned from <a href="https://msdn.microsoft.com/31372688-be81-4883-9fc7-ed3f7b2f7934">ITfCompositionView::GetRange</a>. The range returned by <b>ITfCompositionView::GetRange</b> is not updated until after <b>ITfContextOwnerCompositionSink::OnUpdateComposition</b> returns.




## -see-also




<a href="https://msdn.microsoft.com/1c8aac3e-384e-402e-aae8-11e240083603">ITfCompositionView
      </a>



<a href="https://msdn.microsoft.com/31372688-be81-4883-9fc7-ed3f7b2f7934">
        ITfCompositionView::GetRange
      </a>



<a href="https://msdn.microsoft.com/4fea0a48-df5f-4f34-a3ea-d52883f6f8b1">ITfContextOwnerCompositionSink</a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">
        ITfRange
      </a>
 

 

