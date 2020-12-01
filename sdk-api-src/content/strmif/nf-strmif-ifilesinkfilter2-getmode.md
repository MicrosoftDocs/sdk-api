---
UID: NF:strmif.IFileSinkFilter2.GetMode
title: IFileSinkFilter2::GetMode (strmif.h)
description: The GetMode method retrieves whether the file writer destroys the file when it creates the new one.
helpviewer_keywords: ["GetMode","GetMode method [DirectShow]","GetMode method [DirectShow]","IFileSinkFilter2 interface","IFileSinkFilter2 interface [DirectShow]","GetMode method","IFileSinkFilter2.GetMode","IFileSinkFilter2::GetMode","IFileSinkFilter2GetMode","dshow.ifilesinkfilter2_getmode","strmif/IFileSinkFilter2::GetMode"]
old-location: dshow\ifilesinkfilter2_getmode.htm
tech.root: dshow
ms.assetid: b2a8e34e-a6c1-448b-be6e-31fba9d64f6e
ms.date: 12/05/2018
ms.keywords: GetMode, GetMode method [DirectShow], GetMode method [DirectShow],IFileSinkFilter2 interface, IFileSinkFilter2 interface [DirectShow],GetMode method, IFileSinkFilter2.GetMode, IFileSinkFilter2::GetMode, IFileSinkFilter2GetMode, dshow.ifilesinkfilter2_getmode, strmif/IFileSinkFilter2::GetMode
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IFileSinkFilter2::GetMode
 - strmif/IFileSinkFilter2::GetMode
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
 - IFileSinkFilter2.GetMode
---

# IFileSinkFilter2::GetMode


## -description

The <code>GetMode</code> method retrieves whether the file writer destroys the file when it creates the new one.

## -parameters

### -param pdwFlags [out]

Pointer to the retrieved flags. Currently, the only defined flag is AM_FILE_OVERWRITE, which indicates that the file should be destroyed; zero indicates that the file will be left alone.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter2">IFileSinkFilter2 Interface</a>