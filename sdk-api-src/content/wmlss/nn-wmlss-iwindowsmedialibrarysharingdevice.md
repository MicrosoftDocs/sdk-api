---
UID: NN:wmlss.IWindowsMediaLibrarySharingDevice
title: IWindowsMediaLibrarySharingDevice (wmlss.h)
author: windows-sdk-content
description: The IWindowsMediaLibrarySharingDevice interface defines methods that provide access to an individual media device on the home network.
old-location: wmlss\IWindowsMediaLibrarySharingDeviceInterface.htm
tech.root: WMLSS
ms.assetid: 33fe649b-a688-435c-a019-9c308935532e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWindowsMediaLibrarySharingDevice, IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingDeviceInterface, wmlss/IWindowsMediaLibrarySharingDevice
ms.topic: interface
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
 - IWindowsMediaLibrarySharingDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWindowsMediaLibrarySharingDevice interface


## -description


The <b>IWindowsMediaLibrarySharingDevice</b> interface defines methods that provide access to an individual media device on the home network.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsMediaLibrarySharingDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWindowsMediaLibrarySharingDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bdf06c4-f611-48c8-8289-e51351b234ee">get_Authorization</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the device is  authorized to have access to the current user's media library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdf12bcd-3b41-42a6-818b-26294389d4b3">get_DeviceID</a>
</td>
<td align="left" width="63%">
Retrieves the device ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/771c102e-fa23-44bb-aa93-95f7ae9f5e36">get_Properties</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/b975428c-e518-4bc8-a621-193d510661b0">IWindowsMediaLibrarySharingDeviceProperties</a> interface that represents the collection of all properties for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26ac8f24-d212-4558-a66e-ffe5e90bd73b">put_Authorization</a>
</td>
<td align="left" width="63%">
Authorizes or unauthorizes the device to have access to the current user's media library.

</td>
</tr>
</table> 


## -remarks



To obtain an <b>IWindowsMediaLibrarySharingDevice</b> interface, call the <a href="https://msdn.microsoft.com/38a1f5d2-0347-4564-9403-2bf726198aa6">GetDevice</a> method or the <a href="https://msdn.microsoft.com/1ab420b7-ee40-405f-9125-0f9b3c074ef0">get_Item</a> method of the <a href="https://msdn.microsoft.com/62e1f4d6-5b33-45d7-85d5-bc2c333c63e4">IWindowsMediaLibrarySharingDevices</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/b1508671-fc81-4fcf-a57b-ffbb86b89e73">Windows Media Library Sharing Services</a>
 

 

