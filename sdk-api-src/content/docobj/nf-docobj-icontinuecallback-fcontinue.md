---
UID: NF:docobj.IContinueCallback.FContinue
title: IContinueCallback::FContinue (docobj.h)
description: Indicates whether a generic operation should continue.
helpviewer_keywords: ["FContinue","FContinue method [COM]","FContinue method [COM]","IContinueCallback interface","IContinueCallback interface [COM]","FContinue method","IContinueCallback.FContinue","IContinueCallback::FContinue","_com_icontinuecallback_fcontinue","com.icontinuecallback_fcontinue","docobj/IContinueCallback::FContinue"]
old-location: com\icontinuecallback_fcontinue.htm
tech.root: com
ms.assetid: c84899df-fef1-473d-8278-d715a8ab8ee5
ms.date: 12/05/2018
ms.keywords: FContinue, FContinue method [COM], FContinue method [COM],IContinueCallback interface, IContinueCallback interface [COM],FContinue method, IContinueCallback.FContinue, IContinueCallback::FContinue, _com_icontinuecallback_fcontinue, com.icontinuecallback_fcontinue, docobj/IContinueCallback::FContinue
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.idl
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
 - IContinueCallback::FContinue
 - docobj/IContinueCallback::FContinue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IContinueCallback.FContinue
---

# IContinueCallback::FContinue


## -description

Indicates whether a generic operation should continue.



## -returns

This method can return the following values.

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
Continue the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Cancel the operation as soon as possible.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/docobj/nn-docobj-icontinuecallback">IContinueCallback</a>
