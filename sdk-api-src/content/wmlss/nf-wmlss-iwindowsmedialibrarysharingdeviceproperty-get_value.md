---
UID: NF:wmlss.IWindowsMediaLibrarySharingDeviceProperty.get_Value
title: IWindowsMediaLibrarySharingDeviceProperty::get_Value
author: windows-sdk-content
description: The get_Value method retrieves the value of an individual property of a media device.
old-location: wmlss\IWMLSDevicePropertyget_Value.htm
old-project: wmlss
ms.assetid: b51b794c-eda6-4afe-8bb2-14896f7b8b81
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperty interface [Windows Media Library Sharing Services],get_Value method, IWindowsMediaLibrarySharingDeviceProperty.get_Value, IWindowsMediaLibrarySharingDeviceProperty::get_Value, get_Value, get_Value method [Windows Media Library Sharing Services], get_Value method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDeviceProperty interface, wmlss.IWMLSDevicePropertyget_Value, wmlss/IWindowsMediaLibrarySharingDeviceProperty::get_Value
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
 - IWindowsMediaLibrarySharingDeviceProperty.get_Value
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingDeviceProperty::get_Value


## -description


The <b>get_Value</b> method retrieves the value of an individual property of a media device.


## -parameters




### -param value [out]

A pointer to a <b>VARIANT</b> that receives the property value.


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
 



