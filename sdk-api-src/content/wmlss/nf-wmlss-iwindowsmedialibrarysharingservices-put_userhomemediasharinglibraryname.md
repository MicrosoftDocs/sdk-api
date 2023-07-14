---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingLibraryName
title: IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingLibraryName (wmlss.h)
description: The put_userHomeMediaSharingLibraryName method sets the name of the current user's shared media library.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","put_userHomeMediaSharingLibraryName method","IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingLibraryName","IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingLibraryName","put_userHomeMediaSharingLibraryName","put_userHomeMediaSharingLibraryName method [Windows Media Library Sharing Services]","put_userHomeMediaSharingLibraryName method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSput_userHomeMediaSharingLibraryName","wmlss/IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingLibraryName"]
old-location: wmlss\IWMLSSput_userHomeMediaSharingLibraryName.htm
tech.root: WMLSS
ms.assetid: e3f2863f-4a0d-4896-967f-4daa164bae3b
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],put_userHomeMediaSharingLibraryName method, IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingLibraryName, IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingLibraryName, put_userHomeMediaSharingLibraryName, put_userHomeMediaSharingLibraryName method [Windows Media Library Sharing Services], put_userHomeMediaSharingLibraryName method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSput_userHomeMediaSharingLibraryName, wmlss/IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingLibraryName
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
 - IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingLibraryName
 - wmlss/IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingLibraryName
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
 - IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingLibraryName
---

# IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingLibraryName


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_userHomeMediaSharingLibraryName</b> method sets the name of the current user's shared media library.

## -parameters

### -param libraryName [in]

A <b>BSTR</b> that specifies the library name.

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

