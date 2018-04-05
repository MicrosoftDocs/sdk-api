---
UID: NF:wmlss.IWindowsMediaLibrarySharingDeviceProperties.get_Item
title: IWindowsMediaLibrarySharingDeviceProperties::get_Item method
author: windows-driver-content
description: The get_Item method retrieves an IWindowsMediaLibrarySharingDeviceProperty interface that represents an individual property for a media device.
old-location: wmlss\IWMLSDevicePropertiesget_Item.htm
old-project: WMLSS
ms.assetid: 0c679f64-9d7e-4239-8ee0-2aa5de553c58
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperties, IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services], get_Item method, IWindowsMediaLibrarySharingDeviceProperties::get_Item, get_Item method [Windows Media Library Sharing Services], get_Item method [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingDeviceProperties interface, get_Item,IWindowsMediaLibrarySharingDeviceProperties.get_Item, wmlss.IWMLSDevicePropertiesget_Item, wmlss/IWindowsMediaLibrarySharingDeviceProperties::get_Item
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
req.typenames: WindowsMediaLibrarySharingDeviceAuthorizationStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WMPMediaSharing.dll
api_name:
-	IWindowsMediaLibrarySharingDeviceProperties.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingDeviceProperties::get_Item method


## -description


The <b>get_Item</b> method retrieves an <a href="https://msdn.microsoft.com/7b76cf66-0096-4b63-a30c-2df7d1a14527">IWindowsMediaLibrarySharingDeviceProperty</a> interface that represents an individual property for a media device.


## -parameters




### -param index [in]

The zero-based index of the property in the collection of all properties associated with the media device.


### -param property [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/7b76cf66-0096-4b63-a30c-2df7d1a14527">IWindowsMediaLibrarySharingDeviceProperty</a> interface.


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
 



