---
UID: NF:vss.IVssAsync.Cancel
title: IVssAsync::Cancel (vss.h)
description: The Cancel method cancels an incomplete asynchronous operation.
helpviewer_keywords: ["Cancel","Cancel method [VSS]","Cancel method [VSS]","IVssAsync interface","IVssAsync interface [VSS]","Cancel method","IVssAsync.Cancel","IVssAsync::Cancel","_win32_ivssasync_cancel","base.ivssasync_cancel","vss/IVssAsync::Cancel"]
old-location: base\ivssasync_cancel.htm
tech.root: base
ms.assetid: 8ab44737-114b-4edc-a097-d0fa297f6276
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [VSS], Cancel method [VSS],IVssAsync interface, IVssAsync interface [VSS],Cancel method, IVssAsync.Cancel, IVssAsync::Cancel, _win32_ivssasync_cancel, base.ivssasync_cancel, vss/IVssAsync::Cancel
req.header: vss.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssAsync::Cancel
 - vss/IVssAsync::Cancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssAsync.Cancel
---

# IVssAsync::Cancel


## -description

The 
<b>Cancel</b> method cancels an incomplete asynchronous operation.



## -returns

All calls to 
<b>Cancel</b> for all 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> objects support the following status codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation had been successfully canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_S_ASYNC_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation had been canceled prior to calling this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_S_ASYNC_FINISHED</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation had completed prior to calling this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 

If an operation has completed unsuccessfully before 
<b>Cancel</b> was called, then 
<b>Cancel</b> returns the error that operation encountered.

To obtain a complete list of return values for a specific <b>IVssAsync::Cancel</b>, see the error codes of the method that returned the 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> object.

## -see-also

<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a>



<a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a>
