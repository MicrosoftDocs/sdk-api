---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.showShareMediaCPL
title: IWindowsMediaLibrarySharingServices::showShareMediaCPL (wmlss.h)
description: The showShareMediaCPL method displays the media sharing page in the Control Panel and highlights a specified device.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","showShareMediaCPL method","IWindowsMediaLibrarySharingServices.showShareMediaCPL","IWindowsMediaLibrarySharingServices::showShareMediaCPL","showShareMediaCPL","showShareMediaCPL method [Windows Media Library Sharing Services]","showShareMediaCPL method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSshowShareMediaCPL","wmlss/IWindowsMediaLibrarySharingServices::showShareMediaCPL"]
old-location: wmlss\IWMLSSshowShareMediaCPL.htm
tech.root: WMLSS
ms.assetid: 38d185f3-f5d7-44e8-a36d-673594e3f80c
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],showShareMediaCPL method, IWindowsMediaLibrarySharingServices.showShareMediaCPL, IWindowsMediaLibrarySharingServices::showShareMediaCPL, showShareMediaCPL, showShareMediaCPL method [Windows Media Library Sharing Services], showShareMediaCPL method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSshowShareMediaCPL, wmlss/IWindowsMediaLibrarySharingServices::showShareMediaCPL
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
 - IWindowsMediaLibrarySharingServices::showShareMediaCPL
 - wmlss/IWindowsMediaLibrarySharingServices::showShareMediaCPL
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
 - IWindowsMediaLibrarySharingServices.showShareMediaCPL
---

# IWindowsMediaLibrarySharingServices::showShareMediaCPL


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>showShareMediaCPL</b> method displays the media sharing page in the Control Panel and highlights a specified device.

## -parameters

### -param device [in]

<b>BSTR</b>

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

## -remarks

If <i>device</i> is <b>NULL</b> or if <i>device</i> is an empty <b>BSTR</b>, the focus is set to a default dialog box element. Also, if <i>device</i> is a non-empty <b>BSTR</b> that is not the MAC address of a known device, the focus is set to a default dialog box element.

