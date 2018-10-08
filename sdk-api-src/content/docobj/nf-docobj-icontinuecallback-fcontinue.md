---
UID: NF:docobj.IContinueCallback.FContinue
title: IContinueCallback::FContinue
author: windows-sdk-content
description: Indicates whether a generic operation should continue.
old-location: com\icontinuecallback_fcontinue.htm
tech.root: com
ms.assetid: c84899df-fef1-473d-8278-d715a8ab8ee5
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: FContinue, FContinue method [COM], FContinue method [COM],IContinueCallback interface, IContinueCallback interface [COM],FContinue method, IContinueCallback.FContinue, IContinueCallback::FContinue, _com_icontinuecallback_fcontinue, com.icontinuecallback_fcontinue, docobj/IContinueCallback::FContinue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IContinueCallback.FContinue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContinueCallback::FContinue


## -description


Indicates whether a generic operation should continue.


## -parameters






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




<a href="https://msdn.microsoft.com/55c960be-48e3-42e1-b459-49227be62171">IContinueCallback</a>
 

 

