---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.getAllDevices
title: IWindowsMediaLibrarySharingServices::getAllDevices
author: windows-sdk-content
description: The getAllDevices method retrieves an IWindowsMediaLibrarySharingDevices interface that represents all of the media-sharing client devices on the home network.
old-location: wmlss\IWMLSSgetAllDevices.htm
old-project: WMLSS
ms.assetid: 38dd73b1-fff2-40d3-877f-9ed3c8dfca5b
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],getAllDevices method, IWindowsMediaLibrarySharingServices.getAllDevices, IWindowsMediaLibrarySharingServices::getAllDevices, getAllDevices, getAllDevices method [Windows Media Library Sharing Services], getAllDevices method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSgetAllDevices, wmlss/IWindowsMediaLibrarySharingServices::getAllDevices
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WindowsMediaLibrarySharingDeviceAuthorizationStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WMPMediaSharing.dll
api_name:
-	IWindowsMediaLibrarySharingServices.getAllDevices
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::getAllDevices


## -description


The <b>getAllDevices</b> method retrieves an <a href="https://msdn.microsoft.com/62e1f4d6-5b33-45d7-85d5-bc2c333c63e4">IWindowsMediaLibrarySharingDevices</a> interface that represents all of the media-sharing client devices on the home network.


## -parameters




### -param devices [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/62e1f4d6-5b33-45d7-85d5-bc2c333c63e4">IWindowsMediaLibrarySharingDevices</a> interface.


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
 



