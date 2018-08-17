---
UID: NF:callobj.CoGetInterceptor
title: CoGetInterceptor function
author: windows-sdk-content
description: Instantiates the appropriate interceptor for the specified interface to be intercepted and returns the newly created interceptor.
old-location: com\cogetinterceptor.htm
old-project: com
ms.assetid: d1ffee1d-f907-4091-b993-cf13d8ce616c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CoGetInterceptor, CoGetInterceptor function [COM], _com_CoGetInterceptor, callobj/CoGetInterceptor, com.cogetinterceptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: callobj.h
req.include-header: 
req.redist: 
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
req.typenames: CALLFRAME_COPY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - CoGetInterceptor
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoGetInterceptor function


## -description


Instantiates the appropriate interceptor for the specified interface to be intercepted and returns the newly created interceptor.


## -parameters




### -param iidIntercepted [in]

A reference to the identifier of the interface for which an interceptor is to be returned.


### -param punkOuter [in]

If this parameter is <b>NULL</b>, the object is not being created as part of an aggregate. Otherwise, this parameter is a pointer to the aggregate object's <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface (the controlling <b>IUnknown</b>).  


### -param iid [in]

 A reference to the identifier of the interface desired on the interceptor.


### -param ppv [out]

The address of a pointer variable that receives the interface pointer requested in <i>iid</i>. Upon successful return, **<i>ppv</i> contains the requested interceptor pointer.


## -returns



This function can return the following values. 

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
The function returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms683709(v=VS.85).aspx">ICallFrame</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680109(v=VS.85).aspx">ICallFrameEvents</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693378(v=VS.85).aspx">ICallInterceptor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684028(v=VS.85).aspx">ICallUnmarshal</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678414(v=VS.85).aspx">ISurrogateService</a>
 

 

