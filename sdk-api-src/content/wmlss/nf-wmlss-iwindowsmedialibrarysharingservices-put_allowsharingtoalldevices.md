---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.put_allowSharingToAllDevices
title: IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices
author: windows-sdk-content
description: The put_allowSharingToAllDevices method allows or disallows sharing of the current user's media library with all devices on the home network.
old-location: wmlss\IWMLSSput_allowSharingToAllDevices.htm
old-project: wmlss
ms.assetid: c0dbc9ce-de09-4f60-a975-f09367ba9145
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],put_allowSharingToAllDevices method, IWindowsMediaLibrarySharingServices.put_allowSharingToAllDevices, IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices, put_allowSharingToAllDevices, put_allowSharingToAllDevices method [Windows Media Library Sharing Services], put_allowSharingToAllDevices method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSput_allowSharingToAllDevices, wmlss/IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices
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
 - IWindowsMediaLibrarySharingServices.put_allowSharingToAllDevices
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices


## -description


The <b>put_allowSharingToAllDevices</b> method allows or disallows sharing of the current user's media library with all devices on the home network.


## -parameters




### -param sharingEnabled [in]

A <b>VARIANT_BOOL</b> that specifies whether sharing is allowed (<b>VARIANT_TRUE</b>) or not allowed (<b>VARIANT_FALSE</b>).


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
 



