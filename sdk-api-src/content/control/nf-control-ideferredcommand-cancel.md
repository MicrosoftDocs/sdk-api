---
UID: NF:control.IDeferredCommand.Cancel
title: IDeferredCommand::Cancel (control.h)
description: The Cancel method cancels a command that the application previously queued.helpviewer_keywords: ["Cancel","Cancel method [DirectShow]","Cancel method [DirectShow]","IDeferredCommand interface","IDeferredCommand interface [DirectShow]","Cancel method","IDeferredCommand.Cancel","IDeferredCommand::Cancel","IDeferredCommandCancel","control/IDeferredCommand::Cancel","dshow.ideferredcommand_cancel"]
old-location: dshow\ideferredcommand_cancel.htm
tech.root: DirectShow
ms.assetid: 56618860-3655-42a2-ad74-ef43da08d001
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [DirectShow], Cancel method [DirectShow],IDeferredCommand interface, IDeferredCommand interface [DirectShow],Cancel method, IDeferredCommand.Cancel, IDeferredCommand::Cancel, IDeferredCommandCancel, control/IDeferredCommand::Cancel, dshow.ideferredcommand_cancel
f1_keywords:
- control/IDeferredCommand.Cancel
dev_langs:
- c++
req.header: control.h
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
- IDeferredCommand.Cancel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDeferredCommand::Cancel


## -description



The <code>Cancel</code> method cancels a command that the application previously queued.




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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_ALREADY_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The request was already canceled.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ideferredcommand">IDeferredCommand Interface</a>
 

 

