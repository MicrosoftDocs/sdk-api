---
UID: NF:msctf.ITfThreadMgrEventSink.OnSetFocus
title: ITfThreadMgrEventSink::OnSetFocus method
author: windows-driver-content
description: ITfThreadMgrEventSink::OnSetFocus method
old-location: tsf\itfthreadmgreventsink_onsetfocus.htm
old-project: TSF
ms.assetid: 2c8f2b0a-5b56-4814-bed4-6875a09de176
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfThreadMgrEventSink, ITfThreadMgrEventSink interface [Text Services Framework], OnSetFocus method, ITfThreadMgrEventSink::OnSetFocus, OnSetFocus method [Text Services Framework], OnSetFocus method [Text Services Framework], ITfThreadMgrEventSink interface, OnSetFocus,ITfThreadMgrEventSink.OnSetFocus, _tsf_itfthreadmgreventsink_onsetfocus_ref, msctf/ITfThreadMgrEventSink::OnSetFocus, tsf.itfthreadmgreventsink_onsetfocus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfThreadMgrEventSink.OnSetFocus
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfThreadMgrEventSink::OnSetFocus method


## -description




## -parameters




### -param pdimFocus [in]

Pointer to the document manager receiving the input focus. If no document is receiving the focus, this will be <b>NULL</b>.


### -param pdimPrevFocus [in]

Pointer to the document manager that previously had the input focus. If no document had the focus, this will be <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b437c646-2a15-4ad6-8e7e-3553e7106249">ITfThreadMgr::SetFocus
      </a>



<a href="https://msdn.microsoft.com/be2a3eb1-cb17-4d8b-a44d-ccb33749c8f6">ITfThreadMgrEventSink</a>
 

 

