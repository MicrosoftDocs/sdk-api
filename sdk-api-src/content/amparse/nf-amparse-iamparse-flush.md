---
UID: NF:amparse.IAMParse.Flush
title: IAMParse::Flush (amparse.h)
description: The Flush method clears the current file data to allow for a more rapid switch to a new file.
helpviewer_keywords: ["Flush","Flush method [DirectShow]","Flush method [DirectShow]","IAMParse interface","IAMParse interface [DirectShow]","Flush method","IAMParse.Flush","IAMParse::Flush","IAMParseFlush","amparse/IAMParse::Flush","dshow.iamparse_flush"]
old-location: dshow\iamparse_flush.htm
tech.root: dshow
ms.assetid: 8ff33099-3dc4-4f43-8852-4bd6a8877f29
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [DirectShow], Flush method [DirectShow],IAMParse interface, IAMParse interface [DirectShow],Flush method, IAMParse.Flush, IAMParse::Flush, IAMParseFlush, amparse/IAMParse::Flush, dshow.iamparse_flush
req.header: amparse.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMParse::Flush
 - amparse/IAMParse::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMParse.Flush
---

# IAMParse::Flush


## -description

The <code>Flush</code> method clears the current file data to allow for a more rapid switch to a new file.



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Although this method can make transitions much more immediate, it can also make them appear less seamless.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amparse/nn-amparse-iamparse">IAMParse Interface</a>
