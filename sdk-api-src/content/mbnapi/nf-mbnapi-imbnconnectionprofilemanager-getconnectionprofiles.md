---
UID: NF:mbnapi.IMbnConnectionProfileManager.GetConnectionProfiles
title: IMbnConnectionProfileManager::GetConnectionProfiles
author: windows-sdk-content
description: Gets a list of connection profiles associated with the device.
old-location: mbn\imbnconnectionprofilemanager_getconnectionprofiles.htm
old-project: mbn
ms.assetid: 96752181-1135-4dcf-9c07-056dfbf2ca5f
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetConnectionProfiles, GetConnectionProfiles method [Microsoft Broadband Networks], GetConnectionProfiles method [Microsoft Broadband Networks],IMbnConnectionProfileManager interface, IMbnConnectionProfileManager interface [Microsoft Broadband Networks],GetConnectionProfiles method, IMbnConnectionProfileManager.GetConnectionProfiles, IMbnConnectionProfileManager::GetConnectionProfiles, mbn.imbnconnectionprofilemanager_getconnectionprofiles, mbnapi/IMbnConnectionProfileManager::GetConnectionProfiles
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
 - IMbnConnectionProfileManager.GetConnectionProfiles
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionProfileManager::GetConnectionProfiles


## -description


Gets a list of connection profiles associated with the device.


## -parameters




### -param mbnInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> that represents the device for which the profile request applies.  If this is <b>NULL</b>, the function will return all of the profiles that are present in the system.


### -param connectionProfiles [out, retval]

An array of <a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a> interfaces that represent all the available connection profiles for the device.  If this method returns anything other than <b>S_OK</b>, the array pointer is <b>NULL</b>, otherwise the calling application must eventually free the allocated memory by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=121490">SafeArrayDestroy</a>.


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
The interface is invalid, most likely because the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_READY)</b></dt>
</dl>
</td>
<td width="60%">
The device is not ready.  Unable to obtain the subscriber ID because the device is  not <b>MBN_READY_STATE_INITIALIZED</b>.

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



 When this operation is called for a particular device, it returns a list of profiles which have the same subscriber ID as currently reported by device. The <a href="https://msdn.microsoft.com/9114a3ed-2dc9-4637-b3d5-9430d309e89b">GetSubscriberInformation</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> can be used to obtain the subscriber ID associated with the interface.

A connection profile is associated with the subscriber ID of the device. For GSM devices the subscriber ID is the International Mobile Subscriber Identity (IMSI) of the SIM.  For CDMA devices it is the Mobile Identification Number (MIN) string or the International Roaming MIN (IRM) string. 




## -see-also




<a href="https://msdn.microsoft.com/a55e4183-f914-4064-a391-3bd31ca59160">IMbnConnectionProfileManager</a>
 

 

