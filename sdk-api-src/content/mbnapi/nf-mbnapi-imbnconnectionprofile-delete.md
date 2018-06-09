---
UID: NF:mbnapi.IMbnConnectionProfile.Delete
title: IMbnConnectionProfile::Delete
author: windows-sdk-content
description: Deletes the profile from the system.
old-location: mbn\imbnconnectionprofile_delete.htm
old-project: mbn
ms.assetid: 4de7da76-c873-4a57-a021-17436d1a64a4
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: Delete, Delete method [Microsoft Broadband Networks], Delete method [Microsoft Broadband Networks],IMbnConnectionProfile interface, IMbnConnectionProfile interface [Microsoft Broadband Networks],Delete method, IMbnConnectionProfile.Delete, IMbnConnectionProfile::Delete, mbn.imbnconnectionprofile_delete, mbnapi/IMbnConnectionProfile::Delete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionProfile.Delete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionProfile::Delete


## -description


Deletes the profile from the system.


## -parameters






## -returns



This method can return one of these values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The profile is invalid and likely has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR _NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The profile is invalid and has likely been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
</table>
 




## -remarks



This is an asynchronous operation.  The Mobile Broadband service will notify the calling application by calling the <a href="https://msdn.microsoft.com/30b8c7fb-5a48-4025-aa94-18f17e7c8d19">OnConnectionProfileRemoval</a> method of the <a href="https://msdn.microsoft.com/08ec0bff-898f-4a54-b711-ceae80e7329d">IMbnConnectionProfileManagerEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a>
 

 

