---
UID: NF:msctf.ITfTextLayoutSink.OnLayoutChange
title: ITfTextLayoutSink::OnLayoutChange
author: windows-sdk-content
description: ITfTextLayoutSink::OnLayoutChange method
old-location: tsf\itftextlayoutsink_onlayoutchange.htm
old-project: TSF
ms.assetid: a99313ab-98a7-4fc0-b3ae-78ff26a41d8e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfTextLayoutSink interface [Text Services Framework],OnLayoutChange method, ITfTextLayoutSink.OnLayoutChange, ITfTextLayoutSink::OnLayoutChange, OnLayoutChange, OnLayoutChange method [Text Services Framework], OnLayoutChange method [Text Services Framework],ITfTextLayoutSink interface, _tsf_itftextlayoutsink_onlayoutchange_ref, msctf/ITfTextLayoutSink::OnLayoutChange, tsf.itftextlayoutsink_onlayoutchange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - tiptsf.dll
api_name:
 - ITfTextLayoutSink.OnLayoutChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfTextLayoutSink::OnLayoutChange


## -description




## -parameters




### -param pic [in]

Pointer to the <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface for the context that changed.


### -param lcode [in]

Specifies the <a href="https://msdn.microsoft.com/b9ff6d11-68f2-47c5-b8d7-b3bc2533fdbb">TfLayoutCode</a> element that describes the layout change.


### -param pView [in]

Pointer to the <a href="https://msdn.microsoft.com/302d185d-dab7-4a77-a5cf-da2529d8b24a">ITfContextView</a> interface for the context view in that the layout change occurred.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each context has a default view for which a reference can be obtained using the <a href="https://msdn.microsoft.com/41f7eb74-bca2-4d53-8a70-0b872616fd1b">ITfContext::GetActiveView</a> method. The method returns only the value TF_LC_CHANGE for the <i>lcode</i> parameter for this view, because the values are possible only for multiple views. Because TSF does not support multiple views, this method never receives other values of the <b>TfLayoutCode</b> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/41f7eb74-bca2-4d53-8a70-0b872616fd1b">ITfContext::GetActiveView
      </a>



<a href="https://msdn.microsoft.com/302d185d-dab7-4a77-a5cf-da2529d8b24a">ITfContextView
      </a>



<a href="https://msdn.microsoft.com/370e30a8-6eed-448a-87c7-7fd01e9973c6">ITfTextLayoutSink
      </a>



<a href="https://msdn.microsoft.com/b9ff6d11-68f2-47c5-b8d7-b3bc2533fdbb">TfLayoutCode
      </a>
 

 

