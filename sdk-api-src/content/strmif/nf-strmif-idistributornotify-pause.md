---
UID: NF:strmif.IDistributorNotify.Pause
title: IDistributorNotify::Pause (strmif.h)
description: The Pause method is called when the filter graph is entering a paused state.helpviewer_keywords: ["IDistributorNotify interface [DirectShow]","Pause method","IDistributorNotify.Pause","IDistributorNotify::Pause","IDistributorNotifyPause","Pause","Pause method [DirectShow]","Pause method [DirectShow]","IDistributorNotify interface","dshow.idistributornotify_pause","strmif/IDistributorNotify::Pause"]
old-location: dshow\idistributornotify_pause.htm
tech.root: DirectShow
ms.assetid: d8fcb5c0-4530-4084-adba-170a647588b1
ms.date: 12/05/2018
ms.keywords: IDistributorNotify interface [DirectShow],Pause method, IDistributorNotify.Pause, IDistributorNotify::Pause, IDistributorNotifyPause, Pause, Pause method [DirectShow], Pause method [DirectShow],IDistributorNotify interface, dshow.idistributornotify_pause, strmif/IDistributorNotify::Pause
f1_keywords:
- strmif/IDistributorNotify.Pause
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDistributorNotify.Pause
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDistributorNotify::Pause


## -description



The <code>Pause</code> method is called when the filter graph is entering a paused state.




## -parameters






## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Transition is not complete, but no error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



This method is called before the filters are notified.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idistributornotify">IDistributorNotify Interface</a>
 

 

