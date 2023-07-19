---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.getAllDevices
title: IWindowsMediaLibrarySharingServices::getAllDevices (wmlss.h)
description: The getAllDevices method retrieves an IWindowsMediaLibrarySharingDevices interface that represents all of the media-sharing client devices on the home network.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","getAllDevices method","IWindowsMediaLibrarySharingServices.getAllDevices","IWindowsMediaLibrarySharingServices::getAllDevices","getAllDevices","getAllDevices method [Windows Media Library Sharing Services]","getAllDevices method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSgetAllDevices","wmlss/IWindowsMediaLibrarySharingServices::getAllDevices"]
old-location: wmlss\IWMLSSgetAllDevices.htm
tech.root: WMLSS
ms.assetid: 38dd73b1-fff2-40d3-877f-9ed3c8dfca5b
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],getAllDevices method, IWindowsMediaLibrarySharingServices.getAllDevices, IWindowsMediaLibrarySharingServices::getAllDevices, getAllDevices, getAllDevices method [Windows Media Library Sharing Services], getAllDevices method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSgetAllDevices, wmlss/IWindowsMediaLibrarySharingServices::getAllDevices
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
 - IWindowsMediaLibrarySharingServices::getAllDevices
 - wmlss/IWindowsMediaLibrarySharingServices::getAllDevices
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
 - IWindowsMediaLibrarySharingServices.getAllDevices
---

# IWindowsMediaLibrarySharingServices::getAllDevices


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getAllDevices</b> method retrieves an <a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevices">IWindowsMediaLibrarySharingDevices</a> interface that represents all of the media-sharing client devices on the home network.

## -parameters

### -param devices [out]

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevices">IWindowsMediaLibrarySharingDevices</a> interface.

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