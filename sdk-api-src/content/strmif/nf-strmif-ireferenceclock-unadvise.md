---
UID: NF:strmif.IReferenceClock.Unadvise
title: IReferenceClock::Unadvise
author: windows-sdk-content
description: The Unadvise method removes a pending advise request.
old-location: dshow\ireferenceclock_unadvise.htm
old-project: DirectShow
ms.assetid: 1f032036-4502-473a-93e1-976a66d8bde1
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IReferenceClock interface [DirectShow],Unadvise method, IReferenceClock.Unadvise, IReferenceClock::Unadvise, IReferenceClockUnadvise, Unadvise, Unadvise method [DirectShow], Unadvise method [DirectShow],IReferenceClock interface, dshow.ireferenceclock_unadvise, strmif/IReferenceClock::Unadvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IReferenceClock.Unadvise
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IReferenceClock::Unadvise


## -description



The <code>Unadvise</code> method removes a pending advise request.




## -parameters




### -param dwAdviseCookie [in]

Identifier of the request to remove. Use the value returned by <a href="https://msdn.microsoft.com/22f0c987-a3ae-4d6e-9184-a0a4282340aa">IReferenceClock::AdviseTime</a> or <a href="https://msdn.microsoft.com/c8e2545b-ea3c-441c-8721-e7dec09d100e">IReferenceClock::AdvisePeriodic</a> in the <i>pdwAdviseToken</i> parameter.


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
Not found.

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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock Interface</a>
 

 

