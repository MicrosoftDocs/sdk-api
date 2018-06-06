---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_internetMediaSharingSecurityGroup
title: IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup
author: windows-sdk-content
description: The get_internetMediaSharingSecurityGroup method retrieves the name of the security group that is used to authenticate connections coming in over the Internet.
old-location: wmlss\IWMLSSget_internetMediaSharingSecurityGroup.htm
old-project: WMLSS
ms.assetid: a0085105-7dd5-453d-b372-115d319eb7ac
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_internetMediaSharingSecurityGroup method, IWindowsMediaLibrarySharingServices.get_internetMediaSharingSecurityGroup, IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup, get_internetMediaSharingSecurityGroup, get_internetMediaSharingSecurityGroup method [Windows Media Library Sharing Services], get_internetMediaSharingSecurityGroup method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_internetMediaSharingSecurityGroup, wmlss/IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup
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
 - IWindowsMediaLibrarySharingServices.get_internetMediaSharingSecurityGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup


## -description


The <b>get_internetMediaSharingSecurityGroup</b> method retrieves the name of the security group that is used to authenticate connections coming in over the Internet.


## -parameters




### -param securityGroup [out]

A pointer to a <b>BSTR</b> that receives the name of the security group.


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



The Internet media sharing security group applies only to Windows Home Server. Applications running on other versions of Windows can call <a href="https://msdn.microsoft.com/4195fee6-5a4a-4ed0-b433-99932d28579f">put_internetMediaSharingSecurityGroup</a> and <b>get_internetMediaSharingSecurityGroup</b>, but the calls will have no effect.



