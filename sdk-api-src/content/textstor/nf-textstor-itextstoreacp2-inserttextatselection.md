---
UID: NF:textstor.ITextStoreACP2.InsertTextAtSelection
title: ITextStoreACP2::InsertTextAtSelection
author: windows-sdk-content
description: Inserts text at the insertion point or selection. A caller must have a read/write lock on the document before inserting text.
old-location: tsf\itextstoreacp2_inserttextatselection.htm
tech.root: TSF
ms.assetid: 5e1e0893-53be-4753-ba49-32e69597a130
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],InsertTextAtSelection method, ITextStoreACP2.InsertTextAtSelection, ITextStoreACP2::InsertTextAtSelection, InsertTextAtSelection, InsertTextAtSelection method [Text Services Framework], InsertTextAtSelection method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::InsertTextAtSelection, tsf.itextstoreacp2_inserttextatselection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP2.InsertTextAtSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoreACP2::InsertTextAtSelection


## -description


Inserts text at the insertion point or selection. A caller must have a read/write lock on the document before inserting text.


## -parameters




### -param dwFlags [in]


### -param pchText [in]


### -param cch [in]


### -param pacpStart [out]


### -param pacpEnd [out]


### -param pChange [out]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The values of the <i>pacpStart</i> and the <i>pacpEnd</i> parameters depend upon how the client application inserts text into a document. For example, if the application sets the cursor at the start of the inserted text after text insertion, then the value for the <i>pacpStart</i> and <i>pacpEnd</i> parameters is the same as the <b>acpStart</b> member of the <a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">TS_TEXTCHANGE</a> structure.

Applications should not call the <a href="https://msdn.microsoft.com/ed11ebb8-312b-40c7-90de-f5aa7591afd2">OnTextChange</a> method in response to this method.




## -see-also




<a href="https://msdn.microsoft.com/3d9da4f2-ceb9-4abc-8979-d3756d948a57">Compositions</a>



<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>



<a href="https://msdn.microsoft.com/ed11ebb8-312b-40c7-90de-f5aa7591afd2">OnTextChange</a>



<a href="https://msdn.microsoft.com/adc5c539-fdb1-4829-ad17-2f54ec179c47">TF_IAS_* Constants
      </a>



<a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">TS_TEXTCHANGE</a>
 

 

