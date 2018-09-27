---
UID: NF:mfobjects.IMFAsyncResult.GetStatus
title: IMFAsyncResult::GetStatus
author: windows-sdk-content
description: Returns the status of the asynchronous operation.
old-location: mf\imfasyncresult_getstatus.htm
tech.root: medfound
ms.assetid: ad99f3dd-4885-42e8-8f4e-060d522dde7b
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetStatus, GetStatus method [Media Foundation], GetStatus method [Media Foundation],IMFAsyncResult interface, IMFAsyncResult interface [Media Foundation],GetStatus method, IMFAsyncResult.GetStatus, IMFAsyncResult::GetStatus, ad99f3dd-4885-42e8-8f4e-060d522dde7b, mf.imfasyncresult_getstatus, mfobjects/IMFAsyncResult::GetStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAsyncResult.GetStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAsyncResult::GetStatus


## -description



Returns the status of the asynchronous operation.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The operation completed successfully.

</td>
</tr>
</table>
 




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ea778eaa-6460-4a93-bd6a-1857ea8b6230">Asynchronous Callback Methods</a>



<a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a>
 

 

