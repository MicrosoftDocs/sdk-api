---
UID: NN:contentpartner.IWMPContentPartnerCallback
title: IWMPContentPartnerCallback (contentpartner.h)
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartnercallback.htm
tech.root: WMP
ms.assetid: 3c66052b-2b82-44aa-868d-5d5a4501c457
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPContentPartnerCallback, IWMPContentPartnerCallback interface [Windows Media Player], IWMPContentPartnerCallback interface [Windows Media Player],described, IWMPContentPartnerCallbackInterface, contentpartner/IWMPContentPartnerCallback, wmp.iwmpcontentpartnercallback
ms.topic: interface
f1_keywords: 
 - "contentpartner/IWMPContentPartnerCallback"
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
 - IWMPContentPartnerCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentPartnerCallback interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentPartnerCallback</b> interface provides methods, implemented by Windows Media Player, that a content partner plug-in calls to integrate its catalog and services with the Windows Media Player user interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPContentPartnerCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPContentPartnerCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPContentPartnerCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents">AddListContents</a>
</td>
<td align="left" width="63%">
Adds a set of media items to a list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete">BuyComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that a purchase transaction has been completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-changeview">ChangeView</a>
</td>
<td align="left" width="63%">
Changes the view in Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack">DownloadTrack</a>
</td>
<td align="left" width="63%">
Instructs Windows Media Player to download or not to download a particular media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-getcatalogversion">GetCatalogVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version information for the online store catalog currently in use by Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-getcontentidsinlibrary">GetContentIDsInLibrary</a>
</td>
<td align="left" width="63%">
Retrieves an array of content IDs that represent the music tracks in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-listcontentscomplete">ListContentsComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the content partner plug-in is finished adding content to a list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify">Notify</a>
</td>
<td align="left" width="63%">
Provides notifications from the content partner plug-in to Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete">RefreshLicenseComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a request to update the license for a media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete">SendMessageComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-showpopup">ShowPopup</a>
</td>
<td align="left" width="63%">
Instructs Windows Media Player to display an HTML-based dialog box that hosts a webpage provided by the online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete">UpdateDeviceComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a call to <a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice">IWMPContentPartner::UpdateDevice</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-verifypermissioncomplete">VerifyPermissionComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a call to <a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-verifypermission">IWMPContentPartner::VerifyPermission</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/reference-for-type-1-online-stores">Reference for Type 1 Online Stores</a>
 

 

