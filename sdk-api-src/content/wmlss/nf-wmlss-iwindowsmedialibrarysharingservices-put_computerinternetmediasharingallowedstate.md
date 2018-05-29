---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.put_computerInternetMediaSharingAllowedState
title: IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState
author: windows-sdk-content
description: The put_computerInternetMediaSharingAllowedState method specifies whether media libraries on the computer are allowed to be shared on the Internet.
old-location: wmlss\IWMLSSput_computerInternetMediaSharingAllowedState.htm
old-project: WMLSS
ms.assetid: d41d63d7-2b15-4dd5-bbc1-17696924a624
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],put_computerInternetMediaSharingAllowedState method, IWindowsMediaLibrarySharingServices.put_computerInternetMediaSharingAllowedState, IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState, put_computerInternetMediaSharingAllowedState, put_computerInternetMediaSharingAllowedState method [Windows Media Library Sharing Services], put_computerInternetMediaSharingAllowedState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSput_computerInternetMediaSharingAllowedState, wmlss/IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState
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
-	IWindowsMediaLibrarySharingServices.put_computerInternetMediaSharingAllowedState
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState


## -description


The <b>put_computerInternetMediaSharingAllowedState</b> method specifies whether media libraries on the computer are allowed to be shared on the Internet.


## -parameters




### -param sharingAllowed [in]

A <b>VARIANT_BOOL</b> that specifies whether sharing is allowed (<b>VARIANT_TRUE</b>) or not allowed (<b>VARIANT_FALSE</b>).


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



If home media sharing is not allowed for the computer, Internet media sharing is not allowed for the computer.

If Internet media sharing is not allowed for the computer, none of the users' media libraries are shared on the Internet, regardless of whether individual users have enabled Internet media sharing.

If Internet media sharing is allowed for the computer and a particular user has enabled Internet media sharing, then that user's media library is shared on the Internet.




## -see-also




<a href="https://msdn.microsoft.com/bbec5687-3c77-4385-a9be-74c6d84db962">IWindowsMediaLibrarySharingServices</a>



<a href="https://msdn.microsoft.com/d4c6df42-5bbb-47b0-aedc-ffedd6fe9a8a">IWindowsMediaLibrarySharingServices::get_computerInternetMediaSharingAllowedState</a>
 

 

