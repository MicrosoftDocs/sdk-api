---
UID: NF:strmif.IAMExtTransport.GetChase
title: IAMExtTransport::GetChase
author: windows-sdk-content
description: The GetChase method retrieves the status of chase mode.
old-location: dshow\iamexttransport_getchase.htm
old-project: DirectShow
ms.assetid: 9ef12fa0-2ec9-45e5-9c22-20f810dac73b
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetChase, GetChase method [DirectShow], GetChase method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetChase method, IAMExtTransport.GetChase, IAMExtTransport::GetChase, IAMExtTransportGetChase, dshow.iamexttransport_getchase, strmif/IAMExtTransport::GetChase
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
-	IAMExtTransport.GetChase
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport::GetChase


## -description



The <code>GetChase</code> method retrieves the status of chase mode.



This method is not implemented.


## -parameters




### -param pEnabled [out]

Pointer to a <b>long</b> integer that receives one of the following values:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Chase enabled.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Chase disabled.</td>
</tr>
</table>
 


### -param pOffset [out]

Pointer to a <b>long</b> integer that receives an offset from the present time, indicating the offset that the transport will maintain while playing. The offset is given in the current time format; see <a href="https://msdn.microsoft.com/798fa8d0-3834-4168-86a6-069cae3c3e8e">IAMExtTransport::SetTransportBasicParameters</a> for more information.


### -param phEvent [out]

Pointer to a variable that receives an event handle. The event is signaled when the chase offset is established.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/f8c94e74-e243-4fa9-85e6-8c027b514e4f">IAMExtTransport::SetChase</a>
 

 

