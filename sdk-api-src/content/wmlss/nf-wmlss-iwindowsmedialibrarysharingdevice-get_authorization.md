---
UID: NF:wmlss.IWindowsMediaLibrarySharingDevice.get_Authorization
title: IWindowsMediaLibrarySharingDevice::get_Authorization
author: windows-sdk-content
description: The get_Authorization method retrieves a value that indicates whether the device is authorized to have access to the current user's media library.
old-location: wmlss\IWMLSDeviceget_Authorization.htm
old-project: wmlss
ms.assetid: 0bdf06c4-f611-48c8-8289-e51351b234ee
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services],get_Authorization method, IWindowsMediaLibrarySharingDevice.get_Authorization, IWindowsMediaLibrarySharingDevice::get_Authorization, get_Authorization, get_Authorization method [Windows Media Library Sharing Services], get_Authorization method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDevice interface, wmlss.IWMLSDeviceget_Authorization, wmlss/IWindowsMediaLibrarySharingDevice::get_Authorization
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmlss.h
req.include-header: Wmlss.h
req.redist: 
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
 - IWindowsMediaLibrarySharingDevice.get_Authorization
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingDevice::get_Authorization


## -description


The <b>get_Authorization</b> method retrieves a value that indicates whether the device is  authorized to have access to the current user's media library.


## -parameters




### -param authorization [out]

A pointer to a variable that receives an element of the <a href="https://msdn.microsoft.com/2b858236-32d9-410e-bf57-207a1c44c9d5">WindowsMediaLibrarySharingDeviceAuthorizationStatus</a> enumeration.


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
 



