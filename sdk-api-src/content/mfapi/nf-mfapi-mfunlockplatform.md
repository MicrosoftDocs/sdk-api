---
UID: NF:mfapi.MFUnlockPlatform
title: MFUnlockPlatform function (mfapi.h)
description: Unlocks the Media Foundation platform after it was locked by a call to the MFLockPlatform function.
helpviewer_keywords: ["MFUnlockPlatform","MFUnlockPlatform function [Media Foundation]","d4ce5315-4bb2-4ca4-a9a0-20b638a43040","mf.mfunlockplatform","mfapi/MFUnlockPlatform"]
old-location: mf\mfunlockplatform.htm
tech.root: mf
ms.assetid: d4ce5315-4bb2-4ca4-a9a0-20b638a43040
ms.date: 12/05/2018
ms.keywords: MFUnlockPlatform, MFUnlockPlatform function [Media Foundation], d4ce5315-4bb2-4ca4-a9a0-20b638a43040, mf.mfunlockplatform, mfapi/MFUnlockPlatform
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
 - MFUnlockPlatform
 - mfapi/MFUnlockPlatform
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
 - MFUnlockPlatform
---

# MFUnlockPlatform function


## -description

Unlocks the Media Foundation platform after it was locked by a call to the <a href="/windows/desktop/api/mfapi/nf-mfapi-mflockplatform">MFLockPlatform</a> function.



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

The application must call <b>MFUnlockPlatform</b> once for every call to <a href="/windows/desktop/api/mfapi/nf-mfapi-mflockplatform">MFLockPlatform</a>.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-platform-apis">Media Foundation Platform APIs</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
