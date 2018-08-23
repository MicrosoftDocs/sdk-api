---
UID: NN:wmlss.IWindowsMediaLibrarySharingDeviceProperties
title: IWindowsMediaLibrarySharingDeviceProperties
author: windows-sdk-content
description: The IWindowsMediaLibrarySharingDeviceProperties interface defines methods that provide access to the collection of all properties for an individual media device.
old-location: wmlss\IWindowsMediaLibrarySharingDevicePropertiesInterface.htm
old-project: wmlss
ms.assetid: b975428c-e518-4bc8-a621-193d510661b0
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperties, IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingDevicePropertiesInterface, wmlss/IWindowsMediaLibrarySharingDeviceProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IWindowsMediaLibrarySharingDeviceProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingDeviceProperties interface


## -description


The <b>IWindowsMediaLibrarySharingDeviceProperties</b> interface defines methods that provide access to the collection of all properties for an individual media device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsMediaLibrarySharingDeviceProperties</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingDeviceProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWindowsMediaLibrarySharingDeviceProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd0d1031-875d-4081-b23b-fb2cf77c4f13">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of properties associated with an individual media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c679f64-9d7e-4239-8ee0-2aa5de553c58">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/7b76cf66-0096-4b63-a30c-2df7d1a14527">IWindowsMediaLibrarySharingDeviceProperty</a> interface that represents an individual property for a media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32ae77a2-d80e-4295-9fd2-83b1ad7e8c73">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/7b76cf66-0096-4b63-a30c-2df7d1a14527">IWindowsMediaLibrarySharingDeviceProperty</a> interface that represents an individual property for a media device.

</td>
</tr>
</table> 


## -remarks



To obtain an <b>IWindowsMediaLibrarySharingDeviceProperties</b> interface, call the <a href="https://msdn.microsoft.com/771c102e-fa23-44bb-aa93-95f7ae9f5e36">get_Properties</a> method of the <a href="https://msdn.microsoft.com/33fe649b-a688-435c-a019-9c308935532e">IWindowsMediaLibrarySharingDevice</a> interface.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/b1508671-fc81-4fcf-a57b-ffbb86b89e73">Windows Media Library Sharing Services</a>
 

 

