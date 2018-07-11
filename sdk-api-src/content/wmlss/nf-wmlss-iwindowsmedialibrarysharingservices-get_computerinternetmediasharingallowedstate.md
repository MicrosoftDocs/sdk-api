---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_computerInternetMediaSharingAllowedState
title: IWindowsMediaLibrarySharingServices::get_computerInternetMediaSharingAllowedState
author: windows-sdk-content
description: The get_computerInternetMediaSharingAllowedState method retrieves a value that indicates whether media libraries on the computer are allowed to be shared on the Internet.
old-location: wmlss\IWMLSSget_computerInternetMediaSharingAllowedState.htm
old-project: wmlss
ms.assetid: d4c6df42-5bbb-47b0-aedc-ffedd6fe9a8a
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_computerInternetMediaSharingAllowedState method, IWindowsMediaLibrarySharingServices.get_computerInternetMediaSharingAllowedState, IWindowsMediaLibrarySharingServices::get_computerInternetMediaSharingAllowedState, get_computerInternetMediaSharingAllowedState, get_computerInternetMediaSharingAllowedState method [Windows Media Library Sharing Services], get_computerInternetMediaSharingAllowedState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_computerInternetMediaSharingAllowedState, wmlss/IWindowsMediaLibrarySharingServices::get_computerInternetMediaSharingAllowedState
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMPMediaSharing.dll
api_name:
 - IWindowsMediaLibrarySharingServices.get_computerInternetMediaSharingAllowedState
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::get_computerInternetMediaSharingAllowedState


## -description


The <b>get_computerInternetMediaSharingAllowedState</b> method retrieves a value that indicates whether media libraries on the computer are allowed to be shared on the Internet.



## -parameters




### -param sharingAllowed [out]

Pointer to a <b>VARIANT_BOOL</b> that receives <b>VARIANT_TRUE</b> if media libraries are allowed to be shared and <b>VARIANT_FALSE</b> if media libraries are not allowed to be shared.


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



If home media sharing is not allowed for the computer, Internet media sharing is also not allowed for the computer.

If Internet media sharing is not allowed for the computer, none of the users' media libraries are shared on the Internet, regardless of whether individual users have enabled Internet media sharing.

If Internet media sharing is allowed for the computer and a particular user has enabled Internet media sharing, then that user's media library is shared on the Internet.




## -see-also




<a href="https://msdn.microsoft.com/bbec5687-3c77-4385-a9be-74c6d84db962">IWindowsMediaLibrarySharingServices</a>



<a href="https://msdn.microsoft.com/d41d63d7-2b15-4dd5-bbc1-17696924a624">IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState</a>
 

 

