---
UID: NF:wmlss.IWindowsMediaLibrarySharingDevice.get_DeviceID
title: IWindowsMediaLibrarySharingDevice::get_DeviceID
author: windows-sdk-content
description: The get_DeviceID method retrieves the device ID.
old-location: wmlss\IWMLSDeviceget_DeviceID.htm
old-project: WMLSS
ms.assetid: cdf12bcd-3b41-42a6-818b-26294389d4b3
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services],get_DeviceID method, IWindowsMediaLibrarySharingDevice.get_DeviceID, IWindowsMediaLibrarySharingDevice::get_DeviceID, get_DeviceID, get_DeviceID method [Windows Media Library Sharing Services], get_DeviceID method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDevice interface, wmlss.IWMLSDeviceget_DeviceID, wmlss/IWindowsMediaLibrarySharingDevice::get_DeviceID
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WindowsMediaLibrarySharingDeviceAuthorizationStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMPMediaSharing.dll
api_name:
 - IWindowsMediaLibrarySharingDevice.get_DeviceID
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingDevice::get_DeviceID


## -description


The <b>get_DeviceID</b> method retrieves the device ID.


## -parameters




### -param deviceID [out]

A pointer to a <b>BSTR</b> that receives the device ID.


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
 



