---
UID: NF:strmif.IAMStreamControl.GetInfo
title: IAMStreamControl::GetInfo
author: windows-sdk-content
description: The GetInfo method retrieves information about the current stream-control settings, including the start and stop times.
old-location: dshow\iamstreamcontrol_getinfo.htm
old-project: DirectShow
ms.assetid: 9993534c-ec93-4c15-b977-6a0933d23a72
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetInfo, GetInfo method [DirectShow], GetInfo method [DirectShow],IAMStreamControl interface, IAMStreamControl interface [DirectShow],GetInfo method, IAMStreamControl.GetInfo, IAMStreamControl::GetInfo, IAMStreamControlGetInfo, dshow.iamstreamcontrol_getinfo, strmif/IAMStreamControl::GetInfo
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
-	IAMStreamControl.GetInfo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMStreamControl::GetInfo


## -description



The <code>GetInfo</code> method retrieves information about the current stream-control settings, including the start and stop times.




## -parameters




### -param pInfo [out]

Pointer to an <a href="https://msdn.microsoft.com/63b62f03-1973-41af-b6a4-e1bcb6ab803f">AM_STREAM_INFO</a> structure, allocated by the caller, that receives the current stream-control settings.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/126c7ed7-acc0-4248-a3ab-c91c9f1c5cee">IAMStreamControl Interface</a>
 

 

