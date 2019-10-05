---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_userHomeMediaSharingLibraryName
title: IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingLibraryName (wmlss.h)
author: windows-sdk-content
description: The get_userHomeMediaSharingLibraryName method retrieves the name of the current user's shared media library.
old-location: wmlss\IWMLSSget_userHomeMediaSharingLibraryName.htm
tech.root: WMLSS
ms.assetid: e41d5918-f554-4863-9ea6-11f562ac4d0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_userHomeMediaSharingLibraryName method, IWindowsMediaLibrarySharingServices.get_userHomeMediaSharingLibraryName, IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingLibraryName, get_userHomeMediaSharingLibraryName, get_userHomeMediaSharingLibraryName method [Windows Media Library Sharing Services], get_userHomeMediaSharingLibraryName method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_userHomeMediaSharingLibraryName, wmlss/IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingLibraryName
ms.topic: method
f1_keywords: 
 - "wmlss/IWindowsMediaLibrarySharingServices.get_userHomeMediaSharingLibraryName"
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
 - IWindowsMediaLibrarySharingServices.get_userHomeMediaSharingLibraryName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingLibraryName


## -description


The <b>get_userHomeMediaSharingLibraryName</b> method retrieves the name of the current user's shared media library.


## -parameters




### -param libraryName [out]

Pointer to a <b>BSTR</b> that receives the library name.


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
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingservices">IWindowsMediaLibrarySharingServices</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_userhomemediasharinglibraryname">IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingLibraryName</a>
 

 

