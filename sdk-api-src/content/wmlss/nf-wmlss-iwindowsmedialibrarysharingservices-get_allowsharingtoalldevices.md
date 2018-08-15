---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_allowSharingToAllDevices
title: IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices
author: windows-sdk-content
description: The get_allowSharingToAllDevices method retrieves a value that indicates whether the current user's media library is shared with all devices on the home network.
old-location: wmlss\IWMLSSget_allowSharingToAllDevices.htm
old-project: wmlss
ms.assetid: f166eca1-9413-4f14-be2f-ef433f3e391a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_allowSharingToAllDevices method, IWindowsMediaLibrarySharingServices.get_allowSharingToAllDevices, IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices, get_allowSharingToAllDevices, get_allowSharingToAllDevices method [Windows Media Library Sharing Services], get_allowSharingToAllDevices method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_allowSharingToAllDevices, wmlss/IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices
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
 - IWindowsMediaLibrarySharingServices.get_allowSharingToAllDevices
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices


## -description


The <b>get_allowSharingToAllDevices</b> method retrieves a value that indicates whether the current user's media library is shared with all devices on the home network.


## -parameters




### -param sharingEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> that receives <b>VARIANT_TRUE</b> if the media libray is shared with all devices and <b>VARIANT_FALSE</b> if the media library is not shared with at least one device.


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
 



