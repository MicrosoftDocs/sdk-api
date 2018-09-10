---
UID: NF:wmlss.IWindowsMediaLibrarySharingDevices.GetDevice
title: IWindowsMediaLibrarySharingDevices::GetDevice
author: windows-sdk-content
description: The GetDevice method retrieves an IWindowsMediaLibrarySharingDevice interface that represents an individual media device.
old-location: wmlss\IWMLSDevicesGetDevice.htm
tech.root: WMLSS
ms.assetid: 38a1f5d2-0347-4564-9403-2bf726198aa6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetDevice, GetDevice method [Windows Media Library Sharing Services], GetDevice method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDevices interface, IWindowsMediaLibrarySharingDevices interface [Windows Media Library Sharing Services],GetDevice method, IWindowsMediaLibrarySharingDevices.GetDevice, IWindowsMediaLibrarySharingDevices::GetDevice, wmlss.IWMLSDevicesGetDevice, wmlss/IWindowsMediaLibrarySharingDevices::GetDevice
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
 - IWindowsMediaLibrarySharingDevices.GetDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWindowsMediaLibrarySharingDevices::GetDevice


## -description


The <b>GetDevice</b> method retrieves an <a href="https://msdn.microsoft.com/33fe649b-a688-435c-a019-9c308935532e">IWindowsMediaLibrarySharingDevice</a> interface that represents an individual media device.


## -parameters




### -param deviceID [in]

A <b>BSTR</b> that specifies the device ID.


### -param device [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/33fe649b-a688-435c-a019-9c308935532e">IWindowsMediaLibrarySharingDevice</a> interface.


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
 



