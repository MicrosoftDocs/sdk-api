---
UID: NF:mfobjects.IMFAsyncResult.SetStatus
title: IMFAsyncResult::SetStatus
author: windows-sdk-content
description: Sets the status of the asynchronous operation.
old-location: mf\imfasyncresult_setstatus.htm
old-project: medfound
ms.assetid: 79dec067-ba54-435b-8744-9a6f43dd416d
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 79dec067-ba54-435b-8744-9a6f43dd416d, IMFAsyncResult interface [Media Foundation],SetStatus method, IMFAsyncResult.SetStatus, IMFAsyncResult::SetStatus, SetStatus, SetStatus method [Media Foundation], SetStatus method [Media Foundation],IMFAsyncResult interface, mf.imfasyncresult_setstatus, mfobjects/IMFAsyncResult::SetStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: MF_FILE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAsyncResult.SetStatus
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAsyncResult::SetStatus


## -description



Sets the status of the asynchronous operation.




## -parameters




### -param hrStatus [in]

The status of the asynchronous operation.


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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If you implement an asynchronous method, call <b>SetStatus</b> to set the status code for the operation.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ea778eaa-6460-4a93-bd6a-1857ea8b6230">Asynchronous Callback Methods</a>



<a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a>
 

 

