---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_internetMediaSharingSecurityGroup
title: IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup (wmlss.h)
description: The get_internetMediaSharingSecurityGroup method retrieves the name of the security group that is used to authenticate connections coming in over the Internet.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","get_internetMediaSharingSecurityGroup method","IWindowsMediaLibrarySharingServices.get_internetMediaSharingSecurityGroup","IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup","get_internetMediaSharingSecurityGroup","get_internetMediaSharingSecurityGroup method [Windows Media Library Sharing Services]","get_internetMediaSharingSecurityGroup method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSget_internetMediaSharingSecurityGroup","wmlss/IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup"]
old-location: wmlss\IWMLSSget_internetMediaSharingSecurityGroup.htm
tech.root: WMLSS
ms.assetid: a0085105-7dd5-453d-b372-115d319eb7ac
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_internetMediaSharingSecurityGroup method, IWindowsMediaLibrarySharingServices.get_internetMediaSharingSecurityGroup, IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup, get_internetMediaSharingSecurityGroup, get_internetMediaSharingSecurityGroup method [Windows Media Library Sharing Services], get_internetMediaSharingSecurityGroup method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_internetMediaSharingSecurityGroup, wmlss/IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup
 - wmlss/IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMPMediaSharing.dll
api_name:
 - IWindowsMediaLibrarySharingServices.get_internetMediaSharingSecurityGroup
---

# IWindowsMediaLibrarySharingServices::get_internetMediaSharingSecurityGroup


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

The Internet media sharing security group applies only to Windows Home Server. Applications running on other versions of Windows can call <a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_internetmediasharingsecuritygroup">put_internetMediaSharingSecurityGroup</a> and <b>get_internetMediaSharingSecurityGroup</b>, but the calls will have no effect.