---
UID: NN:wmlss.IWindowsMediaLibrarySharingServices
title: IWindowsMediaLibrarySharingServices (wmlss.h)
description: The IWindowsMediaLibrarySharingServices interface defines methods that configure the sharing of media libraries among users on the local computer, users on the home network, and users on the Internet.
old-location: wmlss\IWindowsMediaLibrarySharingServicesInterface.htm
tech.root: WMLSS
ms.assetid: bbec5687-3c77-4385-a9be-74c6d84db962
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices, IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingServicesInterface, wmlss/IWindowsMediaLibrarySharingServices
f1_keywords:
- wmlss/IWindowsMediaLibrarySharingServices
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
- IWindowsMediaLibrarySharingServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowsMediaLibrarySharingServices interface


## -description


The <b>IWindowsMediaLibrarySharingServices</b> interface defines methods that configure the sharing of media libraries among users on the local computer, users on the home network, and users on the Internet.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsMediaLibrarySharingServices</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingServices</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_allowsharingtoalldevices">get_allowSharingToAllDevices</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the current user's media library is shared  with all devices on the home network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_computerhomemediasharingallowedstate">get_computerHomeMediaSharingAllowedState</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether media libraries on the computer are allowed to be shared on the home network.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_computerinternetmediasharingallowedstate">get_computerInternetMediaSharingAllowedState</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether media libraries on the computer are allowed to be shared on the Internet. 


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_customsettingsapplied">get_customSettingsApplied</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether any custom media-sharing settings are in place for the current user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_internetmediasharingsecuritygroup">get_internetMediaSharingSecurityGroup</a>
</td>
<td align="left" width="63%">
Retrieves the name of the security group that is used to authenticate connections coming in over the Internet.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_userhomemediasharinglibraryname">get_userHomeMediaSharingLibraryName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current user's shared media library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_userhomemediasharingstate">get_userHomeMediaSharingState</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the current user's media library is shared on the home network.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_userinternetmediasharingstate">get_userInternetMediaSharingState</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates whether the current user's media library is shared on the Internet.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-getalldevices">getAllDevices</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevices">IWindowsMediaLibrarySharingDevices</a> interface that represents all of the media-sharing client devices on the home network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_allowsharingtoalldevices">put_allowSharingToAllDevices</a>
</td>
<td align="left" width="63%">
Allows or disallows sharing of the current user's media library with all devices on the home network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_computerhomemediasharingallowedstate">put_computerHomeMediaSharingAllowedState</a>
</td>
<td align="left" width="63%">
Specifies whether media libraries on the computer are allowed to be shared on the home network.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_computerinternetmediasharingallowedstate">put_computerInternetMediaSharingAllowedState</a>
</td>
<td align="left" width="63%">
Specifies whether media libraries on the computer are allowed to be shared on the Internet.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_internetmediasharingsecuritygroup">put_internetMediaSharingSecurityGroup</a>
</td>
<td align="left" width="63%">
Specifies the name of the security group that is used to authenticate connections coming in over the Internet.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_userhomemediasharinglibraryname">put_userHomeMediaSharingLibraryName</a>
</td>
<td align="left" width="63%">
Sets the name of the current user's shared media library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_userhomemediasharingstate">put_userHomeMediaSharingState</a>
</td>
<td align="left" width="63%">
Enables or disables sharing of the current user's media library on the home network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_userinternetmediasharingstate">put_userInternetMediaSharingState</a>
</td>
<td align="left" width="63%">
Enables or disables sharing of the current user's media library on the Internet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-setauthorizationstate">setAuthorizationState</a>
</td>
<td align="left" width="63%">
Enables or disables access to the current user's media library by a specified device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-setdefaultauthorization">setDefaultAuthorization</a>
</td>
<td align="left" width="63%">
Enables or disables access to all users' media libraries by a specified set of devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-showsharemediacpl">showShareMediaCPL</a>
</td>
<td align="left" width="63%">
Displays the media sharing page in the Control Panel and highlights a specified device.

</td>
</tr>
</table> 


## -remarks



To obtain an <b>IWindowsMediaLibrarySharingServices</b> interface, call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create a <b>WindowsMediaLibrarySharingServices</b> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal">Windows Media Library Sharing Services</a>
 

 

