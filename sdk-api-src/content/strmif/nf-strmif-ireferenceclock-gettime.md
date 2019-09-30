---
UID: NF:strmif.IReferenceClock.GetTime
title: IReferenceClock::GetTime (strmif.h)
author: windows-sdk-content
description: The GetTime method retrieves the current reference time.
old-location: dshow\ireferenceclock_gettime.htm
tech.root: DirectShow
ms.assetid: 1fcf8b8a-f449-4f42-8061-cc4116867d9d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTime, GetTime method [DirectShow], GetTime method [DirectShow],IReferenceClock interface, IReferenceClock interface [DirectShow],GetTime method, IReferenceClock.GetTime, IReferenceClock::GetTime, IReferenceClockGetTime, dshow.ireferenceclock_gettime, strmif/IReferenceClock::GetTime
ms.topic: method
f1_keywords: 
 - "strmif/IReferenceClock.GetTime"
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
 - IReferenceClock.GetTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IReferenceClock::GetTime


## -description



The <code>GetTime</code> method retrieves the current reference time.




## -parameters




### -param pTime [out]

Pointer to a variable that receives the current time, in 100-nanosecond units.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returned time is the same as the previous value.

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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock Interface</a>
 

 

