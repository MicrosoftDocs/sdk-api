---
UID: NF:mfidl.IMFSaveJob.EndSave
title: IMFSaveJob::EndSave
author: windows-sdk-content
description: Completes the operation started by IMFSaveJob::BeginSave.
old-location: mf\imfsavejob_endsave.htm
old-project: medfound
ms.assetid: 9d63d7b5-4454-4301-b467-eea82bace6ff
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 9d63d7b5-4454-4301-b467-eea82bace6ff, EndSave, EndSave method [Media Foundation], EndSave method [Media Foundation],IMFSaveJob interface, IMFSaveJob interface [Media Foundation],EndSave method, IMFSaveJob.EndSave, IMFSaveJob::EndSave, mf.imfsavejob_endsave, mfidl/IMFSaveJob::EndSave
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFSaveJob.EndSave
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSaveJob::EndSave


## -description



Completes the operation started by <a href="https://msdn.microsoft.com/ff137b76-2a05-4e58-8d4f-d12cdd89656b">IMFSaveJob::BeginSave</a>.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


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
 




## -see-also




<a href="https://msdn.microsoft.com/0f38fa60-ed04-40c4-9bb0-b6e196cd9586">IMFSaveJob</a>
 

 

