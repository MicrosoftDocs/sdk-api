---
UID: NF:wmlss.IWindowsMediaLibrarySharingDevice.get_Properties
title: IWindowsMediaLibrarySharingDevice::get_Properties
author: windows-sdk-content
description: The get_Properties method retrieves an IWindowsMediaLibrarySharingDeviceProperties interface that represents the collection of all properties for the device.
old-location: wmlss\IWMLSDeviceget_Properties.htm
old-project: WMLSS
ms.assetid: 771c102e-fa23-44bb-aa93-95f7ae9f5e36
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services],get_Properties method, IWindowsMediaLibrarySharingDevice.get_Properties, IWindowsMediaLibrarySharingDevice::get_Properties, get_Properties, get_Properties method [Windows Media Library Sharing Services], get_Properties method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDevice interface, wmlss.IWMLSDeviceget_Properties, wmlss/IWindowsMediaLibrarySharingDevice::get_Properties
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
 - IWindowsMediaLibrarySharingDevice.get_Properties
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingDevice::get_Properties


## -description


The <b>get_Properties</b> method retrieves an <a href="https://msdn.microsoft.com/b975428c-e518-4bc8-a621-193d510661b0">IWindowsMediaLibrarySharingDeviceProperties</a> interface that represents the collection of all properties for the device.


## -parameters




### -param deviceProperties [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/b975428c-e518-4bc8-a621-193d510661b0">IWindowsMediaLibrarySharingDeviceProperties</a> interface.


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
 



