---
UID: NN:wmlss.IWindowsMediaLibrarySharingDeviceProperty
title: IWindowsMediaLibrarySharingDeviceProperty (wmlss.h)

description: The IWindowsMediaLibrarySharingDeviceProperty interface defines methods that provide access to the name and value of an individual property of a media device.
old-location: wmlss\IWindowsMediaLibrarySharingDevicePropertyInterface.htm
tech.root: WMLSS
ms.assetid: 7b76cf66-0096-4b63-a30c-2df7d1a14527

ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperty, IWindowsMediaLibrarySharingDeviceProperty interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingDeviceProperty interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingDevicePropertyInterface, wmlss/IWindowsMediaLibrarySharingDeviceProperty
ms.topic: interface
f1_keywords: 
 - "wmlss/IWindowsMediaLibrarySharingDeviceProperty"
dev_langs:
 - c++
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
 - IWindowsMediaLibrarySharingDeviceProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowsMediaLibrarySharingDeviceProperty interface


## -description


The <b>IWindowsMediaLibrarySharingDeviceProperty</b> interface defines methods that provide access to the name and value of an individual property of a media device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsMediaLibrarySharingDeviceProperty</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingDeviceProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWindowsMediaLibrarySharingDeviceProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdeviceproperty-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the name of an individual property of a media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdeviceproperty-get_value">get_Value</a>
</td>
<td align="left" width="63%">
Retrieves the value of an individual property of a media device.

</td>
</tr>
</table> 


## -remarks



To obtain an <b>IWindowsMediaLibrarySharingDeviceProperty</b> interface, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdeviceproperties-getproperty">GetProperty</a> method or the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdeviceproperties-get_item">get_Item</a> method of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdeviceproperties">IWindowsMediaLibrarySharingDeviceProperties</a> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal">Windows Media Library Sharing Services</a>
 

 

