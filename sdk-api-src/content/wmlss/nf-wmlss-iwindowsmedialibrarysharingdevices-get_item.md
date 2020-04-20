---
UID: NF:wmlss.IWindowsMediaLibrarySharingDevices.get_Item
title: IWindowsMediaLibrarySharingDevices::get_Item (wmlss.h)
description: The get_Item method retrieves an IWindowsMediaLibrarySharingDevice interface that represents an individual media device.helpviewer_keywords: ["IWindowsMediaLibrarySharingDevices interface [Windows Media Library Sharing Services]","get_Item method","IWindowsMediaLibrarySharingDevices.get_Item","IWindowsMediaLibrarySharingDevices::get_Item","get_Item","get_Item method [Windows Media Library Sharing Services]","get_Item method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDevices interface","wmlss.IWMLSDevicesget_Item","wmlss/IWindowsMediaLibrarySharingDevices::get_Item"]
old-location: wmlss\IWMLSDevicesget_Item.htm
tech.root: WMLSS
ms.assetid: 1ab420b7-ee40-405f-9125-0f9b3c074ef0
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDevices interface [Windows Media Library Sharing Services],get_Item method, IWindowsMediaLibrarySharingDevices.get_Item, IWindowsMediaLibrarySharingDevices::get_Item, get_Item, get_Item method [Windows Media Library Sharing Services], get_Item method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDevices interface, wmlss.IWMLSDevicesget_Item, wmlss/IWindowsMediaLibrarySharingDevices::get_Item
f1_keywords:
- wmlss/IWindowsMediaLibrarySharingDevices.get_Item
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
- IWindowsMediaLibrarySharingDevices.get_Item
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowsMediaLibrarySharingDevices::get_Item


## -description


The <b>get_Item</b> method retrieves an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevice">IWindowsMediaLibrarySharingDevice</a> interface that represents an individual media device.


## -parameters




### -param index [in]

The zero-based index of the device in the collection of media devices on the home network.


### -param device [out]

A pointer to a variable that receives a pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevice">IWindowsMediaLibrarySharingDevice</a> interface.


## -returns



This method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevices">IWindowsMediaLibrarySharingDevices</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdevices-get_count">IWindowsMediaLibrarySharingDevices::get_Count</a>
 

 

