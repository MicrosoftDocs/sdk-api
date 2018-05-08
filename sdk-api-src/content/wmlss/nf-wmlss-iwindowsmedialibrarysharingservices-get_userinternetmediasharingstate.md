---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_userInternetMediaSharingState
title: IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState
author: windows-driver-content
description: The get_userInternetMediaSharingState method retrieves a value that indicates whether the current user's media library is shared on the Internet.
old-location: wmlss\IWMLSSget_userInternetMediaSharingState.htm
old-project: WMLSS
ms.assetid: 577fb416-1ff4-4206-8916-9b54577e4cd3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_userInternetMediaSharingState method, IWindowsMediaLibrarySharingServices.get_userInternetMediaSharingState, IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState, get_userInternetMediaSharingState, get_userInternetMediaSharingState method [Windows Media Library Sharing Services], get_userInternetMediaSharingState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_userInternetMediaSharingState, wmlss/IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState
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
req.typenames: WindowsMediaLibrarySharingDeviceAuthorizationStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WMPMediaSharing.dll
api_name:
-	IWindowsMediaLibrarySharingServices.get_userInternetMediaSharingState
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState


## -description


The <b>get_userInternetMediaSharingState</b> method retrieves a value that indicates whether the current user's media library is shared on the Internet.


## -parameters




### -param sharingEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> that receives <b>VARIANT_TRUE</b> if the media library is shared and <b>VARIANT_FALSE</b> if the media library is not shared.


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
 




## -remarks



If Internet media sharing is not allowed for the computer, this method retrieves <b>VARIANT_FALSE</b> regardless of whether Internet media sharing is enabled by the current user.

If Internet media sharing is allowed for the computer and Internet media sharing  is enabled by the current user, this method retrieves <b>VARIANT_TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/bbec5687-3c77-4385-a9be-74c6d84db962">IWindowsMediaLibrarySharingServices</a>



<a href="https://msdn.microsoft.com/9c1ced28-7ed0-4f65-af4d-34774f911621">IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState</a>



<a href="https://msdn.microsoft.com/3d5ff0eb-02e3-4e03-b606-dcc3a1ec6aaf">IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState</a>
 

 

