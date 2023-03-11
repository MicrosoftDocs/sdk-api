---
UID: NF:mfapi.MFShutdown
title: MFShutdown function (mfapi.h)
description: Shuts down the Microsoft Media Foundation platform.
helpviewer_keywords: ["10be2361-b5b4-4c10-92a1-527ca22c74e4","MFShutdown","MFShutdown function [Media Foundation]","mf.mfshutdown","mfapi/MFShutdown"]
old-location: mf\mfshutdown.htm
tech.root: mf
ms.assetid: 10be2361-b5b4-4c10-92a1-527ca22c74e4
ms.date: 12/05/2018
ms.keywords: 10be2361-b5b4-4c10-92a1-527ca22c74e4, MFShutdown, MFShutdown function [Media Foundation], mf.mfshutdown, mfapi/MFShutdown
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFShutdown
 - mfapi/MFShutdown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFShutdown
---

# MFShutdown function


## -description

Shuts down the Microsoft Media Foundation platform. Call this function once for every call to <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a>. Do not call this function from work queue threads.



## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

**MFShutdown** should be called during should be called during app uninitialization and not from static destructors during process exit.


This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/initializing-media-foundation">Initializing Media Foundation</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
