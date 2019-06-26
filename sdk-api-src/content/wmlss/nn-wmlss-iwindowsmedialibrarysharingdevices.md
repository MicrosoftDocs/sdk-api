---
UID: NN:wmlss.IWindowsMediaLibrarySharingDevices
title: IWindowsMediaLibrarySharingDevices (wmlss.h)
author: windows-sdk-content
description: The IWindowsMediaLibrarySharingDevices.
old-location: wmlss\IWindowsMediaLibrarySharingDevicesInterface.htm
tech.root: WMLSS
ms.assetid: 62e1f4d6-5b33-45d7-85d5-bc2c333c63e4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDevices, IWindowsMediaLibrarySharingDevices interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingDevices interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingDevicesInterface, wmlss/IWindowsMediaLibrarySharingDevices
ms.topic: interface
f1_keywords: 
 - "wmlss/IWindowsMediaLibrarySharingDevices"
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
 - IWindowsMediaLibrarySharingDevices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowsMediaLibrarySharingDevices interface


## -description


The <b>IWindowsMediaLibrarySharingDevices</b> interface defines methods that provide access to the collection of media devices on the home network.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsMediaLibrarySharingDevices</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingDevices</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdevices-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of media devices on the home network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdevices-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevice">IWindowsMediaLibrarySharingDevice</a> interface that represents an individual media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdevices-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevice">IWindowsMediaLibrarySharingDevice</a> interface that represents an individual media device.

</td>
</tr>
</table> 


## -remarks



To obtain an <b>IWindowsMediaLibrarySharingDevices</b> interface, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-getalldevices">getAllDevices</a> method of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingservices">IWindowsMediaLibrarySharingServices</a> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal">Windows Media Library Sharing Services</a>
 

 

