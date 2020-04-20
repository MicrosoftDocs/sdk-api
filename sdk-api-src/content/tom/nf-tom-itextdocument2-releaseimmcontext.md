---
UID: NF:tom.ITextDocument2.ReleaseImmContext
title: ITextDocument2::ReleaseImmContext (tom.h)
description: Releases an Input Method Manager (IMM) input context.helpviewer_keywords: ["ITextDocument2 interface [Windows Controls]","ReleaseImmContext method","ITextDocument2.ReleaseImmContext","ITextDocument2::ReleaseImmContext","ReleaseImmContext","ReleaseImmContext method [Windows Controls]","ReleaseImmContext method [Windows Controls]","ITextDocument2 interface","controls.itextdocument2_releaseimmcontext","tom/ITextDocument2::ReleaseImmContext"]
old-location: controls\itextdocument2_releaseimmcontext.htm
tech.root: Controls
ms.assetid: 2172e20b-2343-4a65-a08e-0d8b8c101860
ms.date: 12/05/2018
ms.keywords: ITextDocument2 interface [Windows Controls],ReleaseImmContext method, ITextDocument2.ReleaseImmContext, ITextDocument2::ReleaseImmContext, ReleaseImmContext, ReleaseImmContext method [Windows Controls], ReleaseImmContext method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_releaseimmcontext, tom/ITextDocument2::ReleaseImmContext
f1_keywords:
- tom/ITextDocument2.ReleaseImmContext
dev_langs:
- c++
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msftedit.dll
api_name:
- ITextDocument2.ReleaseImmContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextDocument2::ReleaseImmContext


## -description


Releases an Input Method Manager (IMM) input context.


## -parameters




### -param Context [in]

Type: <b>int64</b>

The IMM input context to release.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument2-getimmcontext">ITextDocument2::GetIMMContext</a>
 

 

