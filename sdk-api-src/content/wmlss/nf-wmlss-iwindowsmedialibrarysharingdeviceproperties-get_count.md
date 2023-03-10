---
UID: NF:wmlss.IWindowsMediaLibrarySharingDeviceProperties.get_Count
title: IWindowsMediaLibrarySharingDeviceProperties::get_Count (wmlss.h)
description: The get_Count method retrieves the number of properties associated with an individual media device.
helpviewer_keywords: ["IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services]","get_Count method","IWindowsMediaLibrarySharingDeviceProperties.get_Count","IWindowsMediaLibrarySharingDeviceProperties::get_Count","get_Count","get_Count method [Windows Media Library Sharing Services]","get_Count method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDeviceProperties interface","wmlss.IWMLSDevicePropertiesget_Count","wmlss/IWindowsMediaLibrarySharingDeviceProperties::get_Count"]
old-location: wmlss\IWMLSDevicePropertiesget_Count.htm
tech.root: WMLSS
ms.assetid: fd0d1031-875d-4081-b23b-fb2cf77c4f13
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services],get_Count method, IWindowsMediaLibrarySharingDeviceProperties.get_Count, IWindowsMediaLibrarySharingDeviceProperties::get_Count, get_Count, get_Count method [Windows Media Library Sharing Services], get_Count method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDeviceProperties interface, wmlss.IWMLSDevicePropertiesget_Count, wmlss/IWindowsMediaLibrarySharingDeviceProperties::get_Count
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWindowsMediaLibrarySharingDeviceProperties::get_Count
 - wmlss/IWindowsMediaLibrarySharingDeviceProperties::get_Count
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMPMediaSharing.dll
api_name:
 - IWindowsMediaLibrarySharingDeviceProperties.get_Count
---

# IWindowsMediaLibrarySharingDeviceProperties::get_Count


## -description

The <b>get_Count</b> method retrieves the number of properties associated with an individual media device.

## -parameters

### -param count [out]

A pointer to a <b>LONG</b> that receives the number of properties.

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

