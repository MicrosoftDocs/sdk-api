---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_userHomeMediaSharingLibraryName
title: IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingLibraryName
author: windows-sdk-content
description: The get_userHomeMediaSharingLibraryName method retrieves the name of the current user's shared media library.
old-location: wmlss\IWMLSSget_userHomeMediaSharingLibraryName.htm
old-project: WMLSS
ms.assetid: e41d5918-f554-4863-9ea6-11f562ac4d0f
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_userHomeMediaSharingLibraryName method, IWindowsMediaLibrarySharingServices.get_userHomeMediaSharingLibraryName, IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingLibraryName, get_userHomeMediaSharingLibraryName, get_userHomeMediaSharingLibraryName method [Windows Media Library Sharing Services], get_userHomeMediaSharingLibraryName method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_userHomeMediaSharingLibraryName, wmlss/IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingLibraryName
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
-	IWindowsMediaLibrarySharingServices.get_userHomeMediaSharingLibraryName
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/bbec5687-3c77-4385-a9be-74c6d84db962">IWindowsMediaLibrarySharingServices</a>



<a href="https://msdn.microsoft.com/e3f2863f-4a0d-4896-967f-4daa164bae3b">IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingLibraryName</a>
 

 

