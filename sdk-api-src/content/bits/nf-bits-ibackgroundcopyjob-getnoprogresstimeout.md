---
UID: NF:bits.IBackgroundCopyJob.GetNoProgressTimeout
title: IBackgroundCopyJob::GetNoProgressTimeout (bits.h)
description: Retrieves the length of time that the service tries to transfer the file after a transient error condition occurs. If there is progress, the timer is reset.
helpviewer_keywords: ["GetNoProgressTimeout","GetNoProgressTimeout method [BITS]","GetNoProgressTimeout method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetNoProgressTimeout method","IBackgroundCopyJob.GetNoProgressTimeout","IBackgroundCopyJob::GetNoProgressTimeout","_drz_ibackgroundcopyjob_getnoprogresstimeout","bits.ibackgroundcopyjob_getnoprogresstimeout","bits/IBackgroundCopyJob::GetNoProgressTimeout"]
old-location: bits\ibackgroundcopyjob_getnoprogresstimeout.htm
tech.root: Bits
ms.assetid: 4881e5f7-a835-40d5-a056-d6b23e3cd84c
ms.date: 12/05/2018
ms.keywords: GetNoProgressTimeout, GetNoProgressTimeout method [BITS], GetNoProgressTimeout method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetNoProgressTimeout method, IBackgroundCopyJob.GetNoProgressTimeout, IBackgroundCopyJob::GetNoProgressTimeout, _drz_ibackgroundcopyjob_getnoprogresstimeout, bits.ibackgroundcopyjob_getnoprogresstimeout, bits/IBackgroundCopyJob::GetNoProgressTimeout
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob::GetNoProgressTimeout
 - bits/IBackgroundCopyJob::GetNoProgressTimeout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetNoProgressTimeout
---

# IBackgroundCopyJob::GetNoProgressTimeout


## -description

Retrieves the length of time that the service tries to transfer the file after a transient error condition occurs. If there is progress, the timer is reset.

## -parameters

### -param Seconds [in]

Length of time, in seconds, that the service tries to transfer the file after a transient error occurs.

## -returns

This method returns the following <b>HRESULT</b> values, as well as others.

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
Time-out was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Must pass the address of <i>pRetryPeriod</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getminimumretrydelay">IBackgroundCopyJob::GetMinimumRetryDelay</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout">IBackgroundCopyJob::SetNoProgressTimeout</a>