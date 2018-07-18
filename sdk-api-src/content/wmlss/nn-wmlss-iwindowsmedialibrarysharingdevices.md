---
UID: NN:wmlss.IWindowsMediaLibrarySharingDevices
title: IWindowsMediaLibrarySharingDevices
author: windows-sdk-content
description: The IWindowsMediaLibrarySharingDevices.
old-location: wmlss\IWindowsMediaLibrarySharingDevicesInterface.htm
old-project: wmlss
ms.assetid: 62e1f4d6-5b33-45d7-85d5-bc2c333c63e4
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IWindowsMediaLibrarySharingDevices, IWindowsMediaLibrarySharingDevices interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingDevices interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingDevicesInterface, wmlss/IWindowsMediaLibrarySharingDevices
ms.prod: windows
ms.technology: windows-sdk
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
 - IWindowsMediaLibrarySharingDevices
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingDevices interface


## -description


The <b>IWindowsMediaLibrarySharingDevices</b> interface defines methods that provide access to the collection of media devices on the home network.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsMediaLibrarySharingDevices</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingDevices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWindowsMediaLibrarySharingDevices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6eb802a3-18a2-4fcf-9be0-fc251860f3ab">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of media devices on the home network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ab420b7-ee40-405f-9125-0f9b3c074ef0">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/33fe649b-a688-435c-a019-9c308935532e">IWindowsMediaLibrarySharingDevice</a> interface that represents an individual media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451305">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/33fe649b-a688-435c-a019-9c308935532e">IWindowsMediaLibrarySharingDevice</a> interface that represents an individual media device.

</td>
</tr>
</table> 


## -remarks



To obtain an <b>IWindowsMediaLibrarySharingDevices</b> interface, call the <a href="https://msdn.microsoft.com/38dd73b1-fff2-40d3-877f-9ed3c8dfca5b">getAllDevices</a> method of the <a href="https://msdn.microsoft.com/bbec5687-3c77-4385-a9be-74c6d84db962">IWindowsMediaLibrarySharingServices</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/b1508671-fc81-4fcf-a57b-ffbb86b89e73">Windows Media Library Sharing Services</a>
 

 

