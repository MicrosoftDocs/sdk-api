---
UID: NF:windows.foundation.IClosable.Close
title: IClosable::IClosable (windows.foundation.h)
description: Performs application-defined tasks associated with freeing, releasing, or resetting allocated resources.
helpviewer_keywords: ["Close","Close method [Windows Runtime]","Close method [Windows Runtime]","IClosable interface","IClosable interface [Windows Runtime]","Close method","IClosable.Close","IClosable.IClosable","IClosable::Close","IClosable::IClosable","windows/IClosable::Close","winrt.iclosable_close"]
old-location: winrt\iclosable_close.htm
tech.root: WinRT
ms.assetid: B08161D3-01D9-4782-A3FA-EAD15DA8B7D9
ms.date: 12/05/2018
ms.keywords: Close, Close method [Windows Runtime], Close method [Windows Runtime],IClosable interface, IClosable interface [Windows Runtime],Close method, IClosable.Close, IClosable.IClosable, IClosable::Close, IClosable::IClosable, windows/IClosable::Close, winrt.iclosable_close
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IClosable::Close
 - windows.foundation/IClosable::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IClosable.Close
---

# IClosable::IClosable


## -description

Performs application-defined tasks associated with freeing, releasing, or resetting allocated resources.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling the <b>Close</b> method more than once has no effect and returns <b>S_OK</b>. 

For info on implementing the <b>Close</b> method, see  the Remarks at <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-iclosable">IClosable</a>.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-iclosable">IClosable</a>
