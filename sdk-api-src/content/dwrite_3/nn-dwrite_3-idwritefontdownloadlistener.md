---
UID: NN:dwrite_3.IDWriteFontDownloadListener
title: IDWriteFontDownloadListener (dwrite_3.h)
description: Application-defined callback interface that receives notifications from the font download queue (IDWriteFontDownloadQueue interface).
helpviewer_keywords: ["IDWriteFontDownloadListener","IDWriteFontDownloadListener interface [Direct Write]","IDWriteFontDownloadListener interface [Direct Write]","described","directwrite.idwritefontdownloadlistener","dwrite_3/IDWriteFontDownloadListener"]
old-location: directwrite\idwritefontdownloadlistener.htm
tech.root: DirectWrite
ms.assetid: 92678d34-9a14-8d58-129c-be31a0963942
ms.date: 12/05/2018
ms.keywords: IDWriteFontDownloadListener, IDWriteFontDownloadListener interface [Direct Write], IDWriteFontDownloadListener interface [Direct Write],described, directwrite.idwritefontdownloadlistener, dwrite_3/IDWriteFontDownloadListener
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontDownloadListener
 - dwrite_3/IDWriteFontDownloadListener
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontDownloadListener
---

# IDWriteFontDownloadListener interface


## -description

 Application-defined callback interface that receives notifications from the font  download queue (<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a> 
  interface). Callbacks will occur on the downloading thread, and objects must be prepared to handle calls on their methods from other threads at any time.

## -inheritance

The <b>IDWriteFontDownloadListener</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontDownloadListener</b> also has these types of members:

