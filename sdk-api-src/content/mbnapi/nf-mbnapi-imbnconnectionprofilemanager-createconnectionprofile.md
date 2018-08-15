---
UID: NF:mbnapi.IMbnConnectionProfileManager.CreateConnectionProfile
title: IMbnConnectionProfileManager::CreateConnectionProfile
author: windows-sdk-content
description: Creates a new connection profile for the device.
old-location: mbn\imbnconnectionprofilemanager_createconnectionprofile.htm
old-project: mbn
ms.assetid: b9c191cc-aa6f-4548-ad4a-f2b9808c5f23
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateConnectionProfile, CreateConnectionProfile method [Microsoft Broadband Networks], CreateConnectionProfile method [Microsoft Broadband Networks],IMbnConnectionProfileManager interface, IMbnConnectionProfileManager interface [Microsoft Broadband Networks],CreateConnectionProfile method, IMbnConnectionProfileManager.CreateConnectionProfile, IMbnConnectionProfileManager::CreateConnectionProfile, mbn.imbnconnectionprofilemanager_createconnectionprofile, mbnapi/IMbnConnectionProfileManager::CreateConnectionProfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
 - IMbnConnectionProfileManager.CreateConnectionProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionProfileManager::CreateConnectionProfile


## -description


Creates a new connection profile for the device.


## -parameters




### -param xmlProfile [in]

A null-terminated string that contains the profile data in XML format compliant with the <a href="https://msdn.microsoft.com/bfec0a1d-de17-4ebd-b9fb-570e230da317">Mobile Broadband Profile Schema Reference</a>.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
A profile with the given name already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_INVALID_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The profile does not conform to the Mobile Broadband profile schema.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The icon file location passed in the profile is not valid or not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_DEFAULT_PROFILE_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The calling application specified the default profile flag in the XML data, however the default profile already exists for the Mobile Broadband device.

</td>
</tr>
</table>
 




## -remarks



This is a synchronous operation. If this function call is successful, then a new profile will be created and the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/94338c8c-2a89-412f-811e-5c50ecd9be70">OnConnectionProfileArrival</a> method of the <a href="https://msdn.microsoft.com/08ec0bff-898f-4a54-b711-ceae80e7329d">IMbnConnectionProfileManagerEvents</a> interface. 


If the icon file location is specified in the profile data then the Mobile Broadband service will copy the icon file from the specified location in its own store. A subsequent query on the <a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a> object for the icon file location will return the file location where the Mobile Broadband service stored the icon file. Whenever a profile is deleted from the system, its icon file is also deleted from the system. The icon file should be in bmp file format file with 32x32 pixel dimensions.





## -see-also




<a href="https://msdn.microsoft.com/a55e4183-f914-4064-a391-3bd31ca59160">IMbnConnectionProfileManager</a>
 

 

