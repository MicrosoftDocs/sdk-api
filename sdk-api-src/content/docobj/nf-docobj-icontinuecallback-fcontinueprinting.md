---
UID: NF:docobj.IContinueCallback.FContinuePrinting
title: IContinueCallback::FContinuePrinting (docobj.h)
author: windows-sdk-content
description: Indicates whether a lengthy printing operation should continue.
old-location: com\icontinuecallback_fcontinueprinting.htm
tech.root: com
ms.assetid: 9031809a-8e5b-48d9-8af9-4a1a07532406
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FContinuePrinting, FContinuePrinting method [COM], FContinuePrinting method [COM],IContinueCallback interface, IContinueCallback interface [COM],FContinuePrinting method, IContinueCallback.FContinuePrinting, IContinueCallback::FContinuePrinting, _com_icontinuecallback_fcontinueprinting, com.icontinuecallback_fcontinueprinting, docobj/IContinueCallback::FContinuePrinting
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
 - IContinueCallback.FContinuePrinting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContinueCallback::FContinuePrinting


## -description


Indicates whether a lengthy printing operation should continue.


## -parameters




### -param nCntPrinted [in]

The total number of pages that have been printed at the time the object receives a call to <b>FContinuePrinting</b>.


### -param nCurPage [in]

The page number of the page being printed at the time the object receives a call to <b>FContinuePrinting</b>.


### -param pwszPrintStatus [in]

A pointer to the message about the current status of the print job. The object being printed may or may not display this message to the user. This parameter can be <b>NULL</b>.


## -returns



This method can return the standard return value E_UNEXPECTED, as well as the following values.

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
Continue the printing operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Cancel the printing operation as soon as possible.

</td>
</tr>
</table>
 




## -remarks



Implementations of <a href="https://msdn.microsoft.com/30554d89-ad80-4d73-b44a-97ae5079feb8">IPrint::Print</a> call this method at periodic intervals during the printing process. The <a href="https://msdn.microsoft.com/eb0d15c0-8a34-4211-b840-29d5862cf767">IPrint</a> implementation should call back at least after printing each page, so that its client can, if necessary, display useful visual feedback to the user. <b>IPrint::Print</b> can call back multiple times with the same <i>nCntPrinted</i> and <i>nCurPage</i> values, which is sometimes useful when a page being printed is complex and it is appropriate to give a user an opportunity to cancel in mid-page.




## -see-also




<a href="https://msdn.microsoft.com/55c960be-48e3-42e1-b459-49227be62171">IContinueCallback</a>



<a href="https://msdn.microsoft.com/eb0d15c0-8a34-4211-b840-29d5862cf767">IPrint</a>
 

 

