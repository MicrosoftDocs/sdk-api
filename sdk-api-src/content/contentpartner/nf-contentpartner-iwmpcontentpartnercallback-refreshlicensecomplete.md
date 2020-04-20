---
UID: NF:contentpartner.IWMPContentPartnerCallback.RefreshLicenseComplete
title: IWMPContentPartnerCallback::RefreshLicenseComplete (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.helpviewer_keywords: ["IWMPContentPartnerCallback interface [Windows Media Player]","RefreshLicenseComplete method","IWMPContentPartnerCallback.RefreshLicenseComplete","IWMPContentPartnerCallback::RefreshLicenseComplete","IWMPContentPartnerCallbackRefreshLicenseComplete","RefreshLicenseComplete","RefreshLicenseComplete method [Windows Media Player]","RefreshLicenseComplete method [Windows Media Player]","IWMPContentPartnerCallback interface","contentpartner/IWMPContentPartnerCallback::RefreshLicenseComplete","wmp.iwmpcontentpartnercallback_refreshlicensecomplete"]
old-location: wmp\iwmpcontentpartnercallback_refreshlicensecomplete.htm
tech.root: WMP
ms.assetid: 426941d9-8d10-4c30-bf2d-cae3f48b51c6
ms.date: 12/05/2018
ms.keywords: IWMPContentPartnerCallback interface [Windows Media Player],RefreshLicenseComplete method, IWMPContentPartnerCallback.RefreshLicenseComplete, IWMPContentPartnerCallback::RefreshLicenseComplete, IWMPContentPartnerCallbackRefreshLicenseComplete, RefreshLicenseComplete, RefreshLicenseComplete method [Windows Media Player], RefreshLicenseComplete method [Windows Media Player],IWMPContentPartnerCallback interface, contentpartner/IWMPContentPartnerCallback::RefreshLicenseComplete, wmp.iwmpcontentpartnercallback_refreshlicensecomplete
f1_keywords:
- contentpartner/IWMPContentPartnerCallback.RefreshLicenseComplete
dev_langs:
- c++
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- contentpartner.h
api_name:
- IWMPContentPartnerCallback.RefreshLicenseComplete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentPartnerCallback::RefreshLicenseComplete


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>RefreshLicenseComplete</b> method notifies Windows Media Player that the online store has finished processing a request to update the license for a media file.




## -parameters




### -param dwCookie [in]

A cookie that represents a request to update a license for a media file. Windows Media Player previously supplied this cookie to the online store's plug-in by calling <a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense">IWMPContentPartner::RefreshLicense</a>.


### -param contentID [in]

The content ID of the media file for which the license update was requested.


### -param hrRefresh [in]

An <b>HRESULT</b> that indicates whether the license update was successful. Any success code indicates that the update succeeded. Any failure code indicates that the update failed.


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



Windows Media Player requests a license update by calling the plug-in's <a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense">RefreshLicense</a> method, which initiates the update and returns immediately. When the online store has finished processing the update request, the plug-in calls <b>RefreshLicenseComplete</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense">IWMPContentPartner::RefreshLicense</a>



<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback Interface</a>
 

 

