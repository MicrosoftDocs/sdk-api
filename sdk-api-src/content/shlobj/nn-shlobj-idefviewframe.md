---
UID: NN:shlobj.IDefViewFrame
title: IDefViewFrame (shlobj.h)
description: Used only for its IUnknown functionality. It has no methods of its own.
helpviewer_keywords: ["IDefViewFrame","IDefViewFrame interface [Windows Shell]","IDefViewFrame interface [Windows Shell]","described","_win32_IDefViewFrame","shell.IDefViewFrame","shlobj/IDefViewFrame"]
old-location: shell\IDefViewFrame.htm
tech.root: shell
ms.assetid: 59dffa62-a26a-4dfa-95be-6b838a2d2903
ms.date: 12/05/2018
ms.keywords: IDefViewFrame, IDefViewFrame interface [Windows Shell], IDefViewFrame interface [Windows Shell],described, _win32_IDefViewFrame, shell.IDefViewFrame, shlobj/IDefViewFrame
req.header: shlobj.h
req.include-header: 
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDefViewFrame
 - shlobj/IDefViewFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDefViewFrame
---

# IDefViewFrame interface


## -description

Used only for its <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> functionality. It has no methods of its own.

## -remarks

<div class="alert"><b>Note</b>  This interface is supported through Windows XP Service Pack 3 (SP3) and Windows Server 2003. It is not supported in Windows Vista and later versions of Windows.</div>
<div> </div>
The IID for this interface is IID_IDefViewFrame. Use the service ID SID_DefView (defined in shlguid.h) in a call to <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">QueryService</a> as shown in this example.

                


``` syntax
HRESULT hr = isp->QueryService(punkSite, SID_DefView, IID_IDefViewFrame, (void**)&pdvf);
```

