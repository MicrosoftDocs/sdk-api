---
UID: NF:mbnapi.IMbnConnectionProfile.UpdateProfile
title: IMbnConnectionProfile::UpdateProfile
author: windows-driver-content
description: Updates the contents of the profile.
old-location: mbn\imbnconnectionprofile_updateprofile.htm
old-project: mbn
ms.assetid: 3243ffec-1897-4f26-853d-81a7198a892d
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnConnectionProfile interface [Microsoft Broadband Networks],UpdateProfile method, IMbnConnectionProfile.UpdateProfile, IMbnConnectionProfile::UpdateProfile, UpdateProfile, UpdateProfile method [Microsoft Broadband Networks], UpdateProfile method [Microsoft Broadband Networks],IMbnConnectionProfile interface, mbn.imbnconnectionprofile_updateprofile, mbnapi/IMbnConnectionProfile::UpdateProfile
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnConnectionProfile.UpdateProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionProfile::UpdateProfile


## -description


Updates the contents of the profile.


## -parameters




### -param strProfile [in]

A string that contains the profile data in XML format compliant with the <a href="https://msdn.microsoft.com/bfec0a1d-de17-4ebd-b9fb-570e230da317">Mobile Broadband Profile Schema Reference</a>.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The profile data specifies an icon file that cannot be found at the indicated location.

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



The data provided by this method complies with the <a href="https://msdn.microsoft.com/bfec0a1d-de17-4ebd-b9fb-570e230da317">Mobile Broadband Profile Schema Reference</a>.

This method should be called when the device for the profile is present in the system.

This is a synchronous operation.  If successful, the Mobile Broadband service will notify the calling application by calling the <a href="https://msdn.microsoft.com/eb113544-0c89-4b38-a2f4-c67c639fe8a3">OnProfileUpdate</a> method of the <a href="https://msdn.microsoft.com/235fa0ef-4fc2-4a36-8ad7-2dceb597498f">IMbnConnectionProfileEvents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a>
 

 

