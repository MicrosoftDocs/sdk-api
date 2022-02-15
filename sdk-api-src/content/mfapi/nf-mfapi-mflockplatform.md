---
UID: NF:mfapi.MFLockPlatform
title: MFLockPlatform function (mfapi.h)
description: Blocks the MFShutdown function.
helpviewer_keywords: ["040742dc-4ba3-4906-8257-65505b2924d5","MFLockPlatform","MFLockPlatform function [Media Foundation]","mf.mflockplatform","mfapi/MFLockPlatform"]
old-location: mf\mflockplatform.htm
tech.root: mf
ms.assetid: 040742dc-4ba3-4906-8257-65505b2924d5
ms.date: 12/05/2018
ms.keywords: 040742dc-4ba3-4906-8257-65505b2924d5, MFLockPlatform, MFLockPlatform function [Media Foundation], mf.mflockplatform, mfapi/MFLockPlatform
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
 - MFLockPlatform
 - mfapi/MFLockPlatform
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
 - MFLockPlatform
---

# MFLockPlatform function


## -description

Blocks the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> function.



## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -remarks

This function prevents work queue threads from being shut down when <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> is called. Use this function to ensure that asynchronous operations complete gracefully before the platform shuts down.

This function holds a lock on the Media Foundation platform. To unlock the platform, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform">MFUnlockPlatform</a>. The application must call <b>MFUnlockPlatform</b> once for every call to <b>MFLockPlatform</b>.

The <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> function blocks until the platform is unlocked, or until a fixed wait period has elapsed. (The wait period is a few seconds.) To avoid memory leaks, the application should unlock the platform before the wait period ends. For example, cancel any asynchronous operations that are waiting to complete and are holding a lock on the platform.

The default implementation of the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface automatically locks the Media Foundation platform when the result object is created. Releasing the interface unlocks the platform. Therefore, in most cases your application does not need to lock the platform directly. For more information, see <a href="/windows/desktop/medfound/work-queues">Work Queues</a>.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-platform-apis">Media Foundation Platform APIs</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
