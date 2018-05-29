---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingState
title: IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState
author: windows-sdk-content
description: The put_userHomeMediaSharingState method enables or disables sharing of the current user's media library on the home network.
old-location: wmlss\IWMLSSput_userHomeMediaSharingState.htm
old-project: WMLSS
ms.assetid: d638da61-8196-4d46-ad98-fd7ab8a19e9b
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],put_userHomeMediaSharingState method, IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingState, IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState, put_userHomeMediaSharingState, put_userHomeMediaSharingState method [Windows Media Library Sharing Services], put_userHomeMediaSharingState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSput_userHomeMediaSharingState, wmlss/IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState
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
-	IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingState
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState


## -description


The <b>put_userHomeMediaSharingState</b> method enables or disables sharing of the current user's media library on the home network.


## -parameters




### -param sharingEnabled

A <b>VARIANT_BOOL</b> that specifies whether sharing is enabled (<b>VARIANT_TRUE</b>) or disabled (<b>VARIANT_FALSE</b>) for the current user.


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



If home media sharing is not allowed for the computer, other users will not have access to the current user's media library, regardless of whether home media sharing is enabled for the current user.



If home media sharing is allowed for the computer and home media sharing is enabled for the current user, other users on the home network will have access to the current user's media library.

<div class="alert"><b>Warning</b>  If home media sharing is enabled for the current user, the computer updates the access control list (ACL) of each file in the user's media library to grant Read access to the NT SERVICE\WMPNetworkSvc account. This behavior might change in future versions of Windows.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/bbec5687-3c77-4385-a9be-74c6d84db962">IWindowsMediaLibrarySharingServices</a>



<a href="https://msdn.microsoft.com/6f56c825-0fdc-4414-aefa-83f8efee2150">IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingState</a>



<a href="https://msdn.microsoft.com/f844f79e-ae6f-4f57-abec-2b6d5951961f">IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingStateAllowed</a>
 

 

