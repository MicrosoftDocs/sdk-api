---
UID: NF:wmlss.IWindowsMediaLibrarySharingDeviceProperties.GetProperty
title: IWindowsMediaLibrarySharingDeviceProperties::GetProperty
author: windows-sdk-content
description: The GetProperty method retrieves an IWindowsMediaLibrarySharingDeviceProperty interface that represents an indivdual property for a media device.
old-location: wmlss\IWMLSDevicePropertiesGetProperty.htm
tech.root: WMLSS
ms.assetid: 32ae77a2-d80e-4295-9fd2-83b1ad7e8c73
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetProperty, GetProperty method [Windows Media Library Sharing Services], GetProperty method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDeviceProperties interface, IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services],GetProperty method, IWindowsMediaLibrarySharingDeviceProperties.GetProperty, IWindowsMediaLibrarySharingDeviceProperties::GetProperty, wmlss.IWMLSDevicePropertiesGetProperty, wmlss/IWindowsMediaLibrarySharingDeviceProperties::GetProperty
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
 - IWindowsMediaLibrarySharingDeviceProperties.GetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWindowsMediaLibrarySharingDeviceProperties::GetProperty


## -description


The <b>GetProperty</b> method retrieves an <a href="https://msdn.microsoft.com/7b76cf66-0096-4b63-a30c-2df7d1a14527">IWindowsMediaLibrarySharingDeviceProperty</a> interface that represents an indivdual property for a media device.


## -parameters




### -param name [in]

A <b>BSTR</b> that specifies the name of the property.


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
 



