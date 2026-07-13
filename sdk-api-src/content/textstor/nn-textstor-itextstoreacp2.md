---
UID: NN:textstor.ITextStoreACP2
title: ITextStoreACP2 (textstor.h)
description: The ITextStoreACP2 interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF.
helpviewer_keywords: ["ITextStoreACP2","ITextStoreACP2 interface [Text Services Framework]","ITextStoreACP2 interface [Text Services Framework]","described","textstor/ITextStoreACP2","tsf.itextstoreacp2"]
old-location: tsf\itextstoreacp2.htm
tech.root: TSF
ms.assetid: c256f1c2-6b67-4417-8707-3490a2c5cb55
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2, ITextStoreACP2 interface [Text Services Framework], ITextStoreACP2 interface [Text Services Framework],described, textstor/ITextStoreACP2, tsf.itextstoreacp2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2
 - textstor/ITextStoreACP2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITextStoreACP2
---

# ITextStoreACP2 interface


## -description

The <b>ITextStoreACP2</b> interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF. An application can obtain an instance of this interface with a call to the <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">CreateContext</a> method. The interface ID is <b>IID_ITextStoreACP2</b>.

This interface exposes text stores through an application character position (ACP) format. Applications that use an anchor-based format should use <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>.

## -inheritance

The <b>ITextStoreACP2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreACP2</b> also has these types of members:

