---
UID: NF:wmlss.IWindowsMediaLibrarySharingDeviceProperty.get_Name
title: IWindowsMediaLibrarySharingDeviceProperty::get_Name
author: windows-sdk-content
description: The get_Name method retrieves the name of an individual property of a media device.
old-location: wmlss\IWMLSDevicePropertyget_Name.htm
old-project: wmlss
ms.assetid: 335e3beb-351e-40ad-b065-7058716180d3
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperty interface [Windows Media Library Sharing Services],get_Name method, IWindowsMediaLibrarySharingDeviceProperty.get_Name, IWindowsMediaLibrarySharingDeviceProperty::get_Name, get_Name, get_Name method [Windows Media Library Sharing Services], get_Name method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDeviceProperty interface, wmlss.IWMLSDevicePropertyget_Name, wmlss/IWindowsMediaLibrarySharingDeviceProperty::get_Name
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
 - IWindowsMediaLibrarySharingDeviceProperty.get_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingDeviceProperty::get_Name


## -description


The <b>get_Name</b> method retrieves the name of an individual property of a media device.


## -parameters




### -param name [out]

A pointer to a <b>BSTR</b> that receives the property name.


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
 



