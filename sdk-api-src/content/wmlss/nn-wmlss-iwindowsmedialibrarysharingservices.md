---
UID: NN:wmlss.IWindowsMediaLibrarySharingServices
title: IWindowsMediaLibrarySharingServices
author: windows-driver-content
description: The IWindowsMediaLibrarySharingServices interface defines methods that configure the sharing of media libraries among users on the local computer, users on the home network, and users on the Internet.
old-location: wmlss\IWindowsMediaLibrarySharingServicesInterface.htm
old-project: WMLSS
ms.assetid: bbec5687-3c77-4385-a9be-74c6d84db962
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IWindowsMediaLibrarySharingServices, IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services], described, wmlss.IWindowsMediaLibrarySharingServicesInterface, wmlss/IWindowsMediaLibrarySharingServices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IWindowsMediaLibrarySharingServices
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices interface


## -description


The <b>IWindowsMediaLibrarySharingServices</b> interface defines methods that configure the sharing of media libraries among users on the local computer, users on the home network, and users on the Internet.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsMediaLibrarySharingServices</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWindowsMediaLibrarySharingServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f166eca1-9413-4f14-be2f-ef433f3e391a">get_allowSharingToAllDevices</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the current user's media library is shared  with all devices on the home network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c1ced28-7ed0-4f65-af4d-34774f911621">get_computerHomeMediaSharingAllowedState</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether media libraries on the computer are allowed to be shared on the home network.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4c6df42-5bbb-47b0-aedc-ffedd6fe9a8a">get_computerInternetMediaSharingAllowedState</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether media libraries on the computer are allowed to be shared on the Internet. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0e4f5b8-2dcc-4e29-b59d-731608e5b8dd">get_customSettingsApplied</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether any custom media-sharing settings are in place for the current user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0085105-7dd5-453d-b372-115d319eb7ac">get_internetMediaSharingSecurityGroup</a>
</td>
<td align="left" width="63%">
Retrieves the name of the security group that is used to authenticate connections coming in over the Internet.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e41d5918-f554-4863-9ea6-11f562ac4d0f">get_userHomeMediaSharingLibraryName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current user's shared media library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f56c825-0fdc-4414-aefa-83f8efee2150">get_userHomeMediaSharingState</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the current user's media library is shared on the home network.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/577fb416-1ff4-4206-8916-9b54577e4cd3">get_userInternetMediaSharingState</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the current user's media library is shared on the Internet.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38dd73b1-fff2-40d3-877f-9ed3c8dfca5b">getAllDevices</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/62e1f4d6-5b33-45d7-85d5-bc2c333c63e4">IWindowsMediaLibrarySharingDevices</a> interface that represents all of the media-sharing client devices on the home network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0dbc9ce-de09-4f60-a975-f09367ba9145">put_allowSharingToAllDevices</a>
</td>
<td align="left" width="63%">
Allows or disallows sharing of the current user's media library with all devices on the home network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f844f79e-ae6f-4f57-abec-2b6d5951961f">put_computerHomeMediaSharingAllowedState</a>
</td>
<td align="left" width="63%">
Specifies whether media libraries on the computer are allowed to be shared on the home network.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d41d63d7-2b15-4dd5-bbc1-17696924a624">put_computerInternetMediaSharingAllowedState</a>
</td>
<td align="left" width="63%">
Specifies whether media libraries on the computer are allowed to be shared on the Internet.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4195fee6-5a4a-4ed0-b433-99932d28579f">put_internetMediaSharingSecurityGroup</a>
</td>
<td align="left" width="63%">
Specifies the name of the security group that is used to authenticate connections coming in over the Internet.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3f2863f-4a0d-4896-967f-4daa164bae3b">put_userHomeMediaSharingLibraryName</a>
</td>
<td align="left" width="63%">
Sets the name of the current user's shared media library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d638da61-8196-4d46-ad98-fd7ab8a19e9b">put_userHomeMediaSharingState</a>
</td>
<td align="left" width="63%">
Enables or disables sharing of the current user's media library on the home network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d5ff0eb-02e3-4e03-b606-dcc3a1ec6aaf">put_userInternetMediaSharingState</a>
</td>
<td align="left" width="63%">
Enables or disables sharing of the current user's media library on the Internet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd67b81c-9810-4f35-b0b2-c471b4747216">setAuthorizationState</a>
</td>
<td align="left" width="63%">
Enables or disables access to the current user's media library by a specified device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7885f571-6b93-47d8-82ab-d998851f1304">setDefaultAuthorization</a>
</td>
<td align="left" width="63%">
Enables or disables access to all users' media libraries by a specified set of devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38d185f3-f5d7-44e8-a36d-673594e3f80c">showShareMediaCPL</a>
</td>
<td align="left" width="63%">
Displays the media sharing page in the Control Panel and highlights a specified device.

</td>
</tr>
</table> 


## -remarks



To obtain an <b>IWindowsMediaLibrarySharingServices</b> interface, call <a href="7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create a <b>WindowsMediaLibrarySharingServices</b> object.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/b1508671-fc81-4fcf-a57b-ffbb86b89e73">Windows Media Library Sharing Services</a>
 

 

