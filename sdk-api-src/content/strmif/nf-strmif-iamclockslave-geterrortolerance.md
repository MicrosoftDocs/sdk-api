---
UID: NF:strmif.IAMClockSlave.GetErrorTolerance
title: IAMClockSlave::GetErrorTolerance
author: windows-sdk-content
description: The GetErrorTolerance method retrieves the audio renderer's rate-matching tolerance.
old-location: dshow\iamclockslave_geterrortolerance.htm
old-project: DirectShow
ms.assetid: a22e17d8-eb96-4e67-bbd7-7c116694c891
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetErrorTolerance, GetErrorTolerance method [DirectShow], GetErrorTolerance method [DirectShow],IAMClockSlave interface, IAMClockSlave interface [DirectShow],GetErrorTolerance method, IAMClockSlave.GetErrorTolerance, IAMClockSlave::GetErrorTolerance, IAMClockSlaveGetErrorTolerance, dshow.iamclockslave_geterrortolerance, strmif/IAMClockSlave::GetErrorTolerance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMClockSlave.GetErrorTolerance
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMClockSlave::GetErrorTolerance


## -description



The <code>GetErrorTolerance</code> method retrieves the audio renderer's rate-matching tolerance.




## -parameters




### -param pdwTolerance [out]

Pointer to a variable that receives the maximum tolerance, in milliseconds.


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
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7b3d0f93-09dd-4a36-a031-70f61402c314">IAMClockSlave Interface</a>
 

 

