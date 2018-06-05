---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_userHomeMediaSharingState
title: IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingState
author: windows-sdk-content
description: The get_userHomeMediaSharingState method retrieves a value that indicates whether the current user's media library is shared on the home network.
old-location: wmlss\IWMLSSget_userHomeMediaSharingState.htm
old-project: WMLSS
ms.assetid: 6f56c825-0fdc-4414-aefa-83f8efee2150
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_userHomeMediaSharingState method, IWindowsMediaLibrarySharingServices.get_userHomeMediaSharingState, IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingState, get_userHomeMediaSharingState, get_userHomeMediaSharingState method [Windows Media Library Sharing Services], get_userHomeMediaSharingState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_userHomeMediaSharingState, wmlss/IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingState
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
tech.root: 
req.typenames: WindowsMediaLibrarySharingDeviceAuthorizationStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WMPMediaSharing.dll
api_name:
-	IWindowsMediaLibrarySharingServices.get_userHomeMediaSharingState
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingState


## -description


The <b>get_userHomeMediaSharingState</b> method retrieves a value that indicates whether the current user's media library is shared on the home network.


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



If home media sharing is not allowed for the computer, this method retrieves <b>VARIANT_FALSE</b> regardless of whether home media sharing is enabled by the current user.

If home media sharing is allowed for the computer and home media sharing is enabled by the current user, this method retrieves <b>VARIANT_TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/bbec5687-3c77-4385-a9be-74c6d84db962">IWindowsMediaLibrarySharingServices</a>



<a href="https://msdn.microsoft.com/9c1ced28-7ed0-4f65-af4d-34774f911621">IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowed</a>



<a href="https://msdn.microsoft.com/d638da61-8196-4d46-ad98-fd7ab8a19e9b">IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState</a>
 

 

