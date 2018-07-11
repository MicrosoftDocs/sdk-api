---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_customSettingsApplied
title: IWindowsMediaLibrarySharingServices::get_customSettingsApplied
author: windows-sdk-content
description: The get_customSettingsApplied method retrieves a value that indicates whether any custom media-sharing settings are in place for the current user.
old-location: wmlss\IWMLSSget_customSettingsApplied.htm
old-project: wmlss
ms.assetid: f0e4f5b8-2dcc-4e29-b59d-731608e5b8dd
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_customSettingsApplied method, IWindowsMediaLibrarySharingServices.get_customSettingsApplied, IWindowsMediaLibrarySharingServices::get_customSettingsApplied, get_customSettingsApplied, get_customSettingsApplied method [Windows Media Library Sharing Services], get_customSettingsApplied method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_customSettingsApplied, wmlss/IWindowsMediaLibrarySharingServices::get_customSettingsApplied
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
 - IWindowsMediaLibrarySharingServices.get_customSettingsApplied
product: Windows
targetos: Windows
req.lib: 
req.dll: WMPMediaSharing.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsMediaLibrarySharingServices::get_customSettingsApplied


## -description


The <b>get_customSettingsApplied</b> method retrieves a value that indicates whether any custom media-sharing settings are in place for the current user.


## -parameters




### -param customSettingsApplied [out]

Pointer to a <b>VARIANT_BOOL</b> that receives <b>VARIANT_TRUE</b> if any custom settings are in place for the current user and <b>VARIANT_FALSE</b> if the default settings are in place for the current user.


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
 



