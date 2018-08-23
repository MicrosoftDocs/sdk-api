---
UID: NN:contentpartner.IWMPContentPartnerCallback
title: IWMPContentPartnerCallback
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartnercallback.htm
old-project: WMP
ms.assetid: 3c66052b-2b82-44aa-868d-5d5a4501c457
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPContentPartnerCallback, IWMPContentPartnerCallback interface [Windows Media Player], IWMPContentPartnerCallback interface [Windows Media Player],described, IWMPContentPartnerCallbackInterface, contentpartner/IWMPContentPartnerCallback, wmp.iwmpcontentpartnercallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: contentpartner.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WMPTransactionType
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
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentPartnerCallback interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentPartnerCallback</b> interface provides methods, implemented by Windows Media Player, that a content partner plug-in calls to integrate its catalog and services with the Windows Media Player user interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPContentPartnerCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IWMPContentPartnerCallback</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563143(v=VS.85).aspx">AddListContents</a>
</td>
<td align="left" width="63%">
Adds a set of media items to a list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563144(v=VS.85).aspx">BuyComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that a purchase transaction has been completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563145(v=VS.85).aspx">ChangeView</a>
</td>
<td align="left" width="63%">
Changes the view in Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563146(v=VS.85).aspx">DownloadTrack</a>
</td>
<td align="left" width="63%">
Instructs Windows Media Player to download or not to download a particular media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563147(v=VS.85).aspx">GetCatalogVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version information for the online store catalog currently in use by Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563148(v=VS.85).aspx">GetContentIDsInLibrary</a>
</td>
<td align="left" width="63%">
Retrieves an array of content IDs that represent the music tracks in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563149(v=VS.85).aspx">ListContentsComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the content partner plug-in is finished adding content to a list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563150(v=VS.85).aspx">Notify</a>
</td>
<td align="left" width="63%">
Provides notifications from the content partner plug-in to Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563151(v=VS.85).aspx">RefreshLicenseComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a request to update the license for a media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563152(v=VS.85).aspx">SendMessageComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563153(v=VS.85).aspx">ShowPopup</a>
</td>
<td align="left" width="63%">
Instructs Windows Media Player to display an HTML-based dialog box that hosts a webpage provided by the online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563154(v=VS.85).aspx">UpdateDeviceComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a call to <a href="https://msdn.microsoft.com/en-us/library/Dd563177(v=VS.85).aspx">IWMPContentPartner::UpdateDevice</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563155(v=VS.85).aspx">VerifyPermissionComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a call to <a href="https://msdn.microsoft.com/en-us/library/Dd563178(v=VS.85).aspx">IWMPContentPartner::VerifyPermission</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd564243(v=VS.85).aspx">Reference for Type 1 Online Stores</a>
 

 

