---
UID: NN:contentpartner.IWMPContentPartner
title: IWMPContentPartner (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartner.htm
tech.root: WMP
ms.assetid: 2078ebd4-3570-4c39-9081-1b55d9e8286f
ms.date: 12/05/2018
ms.keywords: IWMPContentPartner, IWMPContentPartner interface [Windows Media Player], IWMPContentPartner interface [Windows Media Player],described, IWMPContentPartnerInterface, contentpartner/IWMPContentPartner, wmp.iwmpcontentpartner
f1_keywords:
- contentpartner/IWMPContentPartner
dev_langs:
- c++
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
- IWMPContentPartner
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentPartner interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentPartner</b> interface provides methods that Windows Media Player calls to integrate its user interface with an online store's catalog and services. This interface is implemented by a content partner plug-in, which is provided by the online store.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPContentPartner</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPContentPartner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPContentPartner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate">Authenticate</a>
</td>
<td align="left" width="63%">
Initiates an attempt to authenticate the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy">Buy</a>
</td>
<td align="left" width="63%">
Initiates the purchase of digital media content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent">CanBuySilent</a>
</td>
<td align="left" width="63%">
Calculates the total price of a purchase and determines whether the purchase can proceed without displaying a dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-comparecontainerlistprices">CompareContainerListPrices</a>
</td>
<td align="left" width="63%">
Compares the price of two content container lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download">Download</a>
</td>
<td align="left" width="63%">
Initiates the download of a set of media items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete">DownloadTrackComplete</a>
</td>
<td align="left" width="63%">
Notifies the content partner plug-in that Windows Media Player has finished downloading a track or that the download attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl">GetCatalogURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL from which to retrieve an update to the online store's current catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands">GetCommands</a>
</td>
<td align="left" width="63%">
Retrieves context menu commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo">GetContentPartnerInfo</a>
</td>
<td align="left" width="63%">
Retrieves specific information about the online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo">GetItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves information (for example, a URL or a caption) related to an item owned by an online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">GetListContents</a>
</td>
<td align="left" width="63%">
Initiates the retrieval of a dynamic list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl">GetStreamingURL</a>
</td>
<td align="left" width="63%">
Retrieves the streaming URL of a track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate">GetTemplate</a>
</td>
<td align="left" width="63%">
Retrieves the URL of the discovery page to be displayed when the library view changes in Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand">InvokeCommand</a>
</td>
<td align="left" width="63%">
Invokes a context menu command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login">Login</a>
</td>
<td align="left" width="63%">
Logs the user in to the online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout">Logout</a>
</td>
<td align="left" width="63%">
Ends the user's online store session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify">Notify</a>
</td>
<td align="left" width="63%">
Provides the content partner plug-in with event notifications from Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense">RefreshLicense</a>
</td>
<td align="left" width="63%">
Initiates the update of a license for the specified media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage">SendMessage</a>
</td>
<td align="left" width="63%">
Enables discovery pages to send messages to the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback">SetCallback</a>
</td>
<td align="left" width="63%">
Provides the plug-in with a pointer for calling Windows Media Player methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-stationevent">StationEvent</a>
</td>
<td align="left" width="63%">
Notifies the plug-in of events during playback of a Windows Media metafile playlist (ASX).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice">UpdateDevice</a>
</td>
<td align="left" width="63%">
Notifies the content-partner plug-in that a portable device is being synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-verifypermission">VerifyPermission</a>
</td>
<td align="left" width="63%">
Initiates the process of verifying permission for Windows Media Player to perform an action.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/reference-for-type-1-online-stores">Reference for Type 1 Online Stores</a>
 

 

