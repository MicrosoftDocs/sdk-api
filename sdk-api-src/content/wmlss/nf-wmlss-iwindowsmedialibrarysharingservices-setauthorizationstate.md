---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.setAuthorizationState
title: IWindowsMediaLibrarySharingServices::setAuthorizationState
author: windows-sdk-content
description: The setAuthorizationState method enables or disables access to the current user's media library by a specified device.
old-location: wmlss\IWMLSSsetAuthorizationState.htm
old-project: WMLSS
ms.assetid: bd67b81c-9810-4f35-b0b2-c471b4747216
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],setAuthorizationState method, IWindowsMediaLibrarySharingServices.setAuthorizationState, IWindowsMediaLibrarySharingServices::setAuthorizationState, setAuthorizationState, setAuthorizationState method [Windows Media Library Sharing Services], setAuthorizationState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSsetAuthorizationState, wmlss/IWindowsMediaLibrarySharingServices::setAuthorizationState
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
-	IWindowsMediaLibrarySharingServices.setAuthorizationState
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::setAuthorizationState


## -description


The <b>setAuthorizationState</b> method enables or disables access to the current user's media library by  a specified device.


## -parameters




### -param MACAddress [in]

A <b>BSTR</b> that specifies the MAC address of the device for which access will be enabled or disabled.


### -param authorizationState [in]

A <b>VARIANT_BOOL</b> that specifies whether access by the device is enabled (<b>VARIANT_TRUE</b>) or disabled (<b>VARIANT_FALSE</b>).


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



<a href="https://msdn.microsoft.com/7885f571-6b93-47d8-82ab-d998851f1304">IWindowsMediaLibrarySharingServices::setDefaultAuthorization</a>
 

 

