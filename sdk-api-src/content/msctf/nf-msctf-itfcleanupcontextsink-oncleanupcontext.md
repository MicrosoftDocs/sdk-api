---
UID: NF:msctf.ITfCleanupContextSink.OnCleanupContext
title: ITfCleanupContextSink::OnCleanupContext
author: windows-sdk-content
description: ITfCleanupContextSink::OnCleanupContext method
old-location: tsf\itfcleanupcontextsink_oncleanupcontext.htm
tech.root: TSF
ms.assetid: 6af597e6-f997-4b28-8994-a8dbabcaaa68
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITfCleanupContextSink interface [Text Services Framework],OnCleanupContext method, ITfCleanupContextSink.OnCleanupContext, ITfCleanupContextSink::OnCleanupContext, OnCleanupContext, OnCleanupContext method [Text Services Framework], OnCleanupContext method [Text Services Framework],ITfCleanupContextSink interface, _tsf_itfcleanupcontextsink_oncleanupcontext_ref, msctf/ITfCleanupContextSink::OnCleanupContext, tsf.itfcleanupcontextsink_oncleanupcontext
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
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfCleanupContextSink.OnCleanupContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCleanupContextSink::OnCleanupContext


## -description




## -parameters




### -param ecWrite [in]

Contains a <a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">TfEditCookie</a> value that identifies the edit context cleaned up. The edit context is guaranteed to have a read/write lock.


### -param pic [in]

Pointer to an <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface that represents the context cleaned up.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A context cleanup occurs when:

<ul>
<li>The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.</li>
<li>
<a href="https://msdn.microsoft.com/7293fbfa-c385-4713-80b2-760e54dbf4c1">ITfThreadMgr::Deactivate
            </a> is called while a context is still on the context stack.</li>
</ul>
This method provides the text service with a final opportunity to modify the text or properties within the context. For example, if the text service currently has a composition open when the context cleanup occurs. This method enables the text service to close the composition before the context is destroyed.

The TSF manager automatically releases all properties, including custom properties, when a context is removed from the context stack. Therefore, it is unnecessary for a text service to release its properties in response to this event.




## -see-also




<a href="https://msdn.microsoft.com/f88ebef7-2796-4076-892f-28fac6e143de">ITfCleanupContextSink</a>



<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">TfEditCookie
      </a>
 

 

