---
UID: NF:vss.IVssAsync.Wait
title: IVssAsync::Wait (vss.h)
description: The Wait method waits until an incomplete asynchronous operation finishes.
helpviewer_keywords: ["IVssAsync interface [VSS]","Wait method","IVssAsync.Wait","IVssAsync::Wait","Wait","Wait method [VSS]","Wait method [VSS]","IVssAsync interface","_win32_ivssasync_wait","base.ivssasync_wait","vss/IVssAsync::Wait"]
old-location: base\ivssasync_wait.htm
tech.root: base
ms.assetid: 27be3bb2-de37-47d1-a2da-7b253ace1199
ms.date: 12/05/2018
ms.keywords: IVssAsync interface [VSS],Wait method, IVssAsync.Wait, IVssAsync::Wait, Wait, Wait method [VSS], Wait method [VSS],IVssAsync interface, _win32_ivssasync_wait, base.ivssasync_wait, vss/IVssAsync::Wait
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
 - IVssAsync::Wait
 - vss/IVssAsync::Wait
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
 - IVssAsync.Wait
---

# IVssAsync::Wait


## -description

The 
<b>Wait</b> method waits until an incomplete asynchronous operation finishes.

## -parameters

### -param dwMilliseconds [in]

Length of time, in milliseconds, that the method will wait for an asynchronous process to return before timing out. 




The default value for this argument is INFINITE.

<b>Windows Server 2003:  </b>This parameter is reserved and must be INFINITE. If any other value is specified for this parameter, the call to <b>Wait</b> fails with E_INVALIDARG.

<b>Windows XP:  </b>This method has no parameters.

## -returns

All calls to 
<b>Wait</b> for all 
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
The wait operation was successful. Call 
<a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a> to determine the final status of the asynchronous operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The wait operation failed because the user did not have the correct privileges.

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
 

If an operation fails while being waited on, 
<b>Wait</b> returns the error that operation encountered.

To obtain a complete list of return values for a specific <b>Wait</b>, see the error codes of the method that returned the 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> object.

## -remarks

This method can succeed even if the method that returns it failed.

## -see-also

<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a>



<a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a>