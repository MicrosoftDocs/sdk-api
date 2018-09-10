---
UID: NF:wmlss.IWindowsMediaLibrarySharingDevice.put_Authorization
title: IWindowsMediaLibrarySharingDevice::put_Authorization
author: windows-sdk-content
description: The put_Authorization method authorizes or unauthorizes the device to have access to the current user's media library.
old-location: wmlss\IWMLSDeviceput_Authorization.htm
tech.root: WMLSS
ms.assetid: 26ac8f24-d212-4558-a66e-ffe5e90bd73b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services],put_Authorization method, IWindowsMediaLibrarySharingDevice.put_Authorization, IWindowsMediaLibrarySharingDevice::put_Authorization, put_Authorization, put_Authorization method [Windows Media Library Sharing Services], put_Authorization method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDevice interface, wmlss.IWMLSDeviceput_Authorization, wmlss/IWindowsMediaLibrarySharingDevice::put_Authorization
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmlss.h
req.include-header: Wmlss.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMPMediaSharing.dll
api_name:
 - IWindowsMediaLibrarySharingDevice.put_Authorization
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWindowsMediaLibrarySharingDevice::put_Authorization


## -description


The <b>put_Authorization</b> method authorizes or unauthorizes the device to have access to the current user's media library.


## -parameters




### -param authorization [in]

An element of the <a href="https://msdn.microsoft.com/2b858236-32d9-410e-bf57-207a1c44c9d5">WindowsMediaLibrarySharingDeviceAuthorizationStatus</a> enumeration that specifies whether the device is authorized (<b>DEVICE_AUTHORIZATION_ALLOWED</b>) or unauthorized (<b>DEVICE_AUTHORIZATION_DENIED</b>) to have access to the current user's media library.


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
 



