---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_customSettingsApplied
title: IWindowsMediaLibrarySharingServices::get_customSettingsApplied (wmlss.h)
description: The get_customSettingsApplied method retrieves a value that indicates whether any custom media-sharing settings are in place for the current user.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","get_customSettingsApplied method","IWindowsMediaLibrarySharingServices.get_customSettingsApplied","IWindowsMediaLibrarySharingServices::get_customSettingsApplied","get_customSettingsApplied","get_customSettingsApplied method [Windows Media Library Sharing Services]","get_customSettingsApplied method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSget_customSettingsApplied","wmlss/IWindowsMediaLibrarySharingServices::get_customSettingsApplied"]
old-location: wmlss\IWMLSSget_customSettingsApplied.htm
tech.root: WMLSS
ms.assetid: f0e4f5b8-2dcc-4e29-b59d-731608e5b8dd
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_customSettingsApplied method, IWindowsMediaLibrarySharingServices.get_customSettingsApplied, IWindowsMediaLibrarySharingServices::get_customSettingsApplied, get_customSettingsApplied, get_customSettingsApplied method [Windows Media Library Sharing Services], get_customSettingsApplied method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_customSettingsApplied, wmlss/IWindowsMediaLibrarySharingServices::get_customSettingsApplied
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
 - IWindowsMediaLibrarySharingServices::get_customSettingsApplied
 - wmlss/IWindowsMediaLibrarySharingServices::get_customSettingsApplied
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
 - IWindowsMediaLibrarySharingServices.get_customSettingsApplied
---

# IWindowsMediaLibrarySharingServices::get_customSettingsApplied


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_customSettingsApplied</b> method retrieves a value that indicates whether any custom media-sharing settings are in place for the current user.

## -parameters

### -param customSettingsApplied [out]

Pointer to a <b>VARIANT_BOOL</b> that receives <b>VARIANT_TRUE</b> if any custom settings are in place for the current user and <b>VARIANT_FALSE</b> if the default settings are in place for the current user.

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

