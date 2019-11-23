---
UID: NN:wmlss.IWindowsMediaLibrarySharingDeviceProperties
title: IWindowsMediaLibrarySharingDeviceProperties (wmlss.h)

description: The IWindowsMediaLibrarySharingDeviceProperties interface defines methods that provide access to the collection of all properties for an individual media device.
old-location: wmlss\IWindowsMediaLibrarySharingDevicePropertiesInterface.htm
tech.root: WMLSS
ms.assetid: b975428c-e518-4bc8-a621-193d510661b0

ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperties, IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingDevicePropertiesInterface, wmlss/IWindowsMediaLibrarySharingDeviceProperties
ms.topic: interface
f1_keywords: 
 - "wmlss/IWindowsMediaLibrarySharingDeviceProperties"
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
 - IWindowsMediaLibrarySharingDeviceProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowsMediaLibrarySharingDeviceProperties interface


## -description


The <b>IWindowsMediaLibrarySharingDeviceProperties</b> interface defines methods that provide access to the collection of all properties for an individual media device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsMediaLibrarySharingDeviceProperties</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingDeviceProperties</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371944(v=vs.85)">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of properties associated with an individual media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdeviceproperties-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdeviceproperty">IWindowsMediaLibrarySharingDeviceProperty</a> interface that represents an individual property for a media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdeviceproperties-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdeviceproperty">IWindowsMediaLibrarySharingDeviceProperty</a> interface that represents an individual property for a media device.

</td>
</tr>
</table> 


## -remarks



To obtain an <b>IWindowsMediaLibrarySharingDeviceProperties</b> interface, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdevice-get_properties">get_Properties</a> method of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevice">IWindowsMediaLibrarySharingDevice</a> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal">Windows Media Library Sharing Services</a>
 

 

