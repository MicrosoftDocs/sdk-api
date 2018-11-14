---
UID: NN:contentpartner.IWMPContentPartnerCallback
title: IWMPContentPartnerCallback
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartnercallback.htm
tech.root: WMP
ms.assetid: 3c66052b-2b82-44aa-868d-5d5a4501c457
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPContentPartnerCallback, IWMPContentPartnerCallback interface [Windows Media Player], IWMPContentPartnerCallback interface [Windows Media Player],described, IWMPContentPartnerCallbackInterface, contentpartner/IWMPContentPartnerCallback, wmp.iwmpcontentpartnercallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IWMPContentPartnerCallback interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentPartnerCallback</b> interface provides methods, implemented by Windows Media Player, that a content partner plug-in calls to integrate its catalog and services with the Windows Media Player user interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPContentPartnerCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPContentPartnerCallback</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/22d28495-310e-4f3d-a0e3-8f6679c78c40">AddListContents</a>
</td>
<td align="left" width="63%">
Adds a set of media items to a list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e9ab15f-3418-472d-afc4-0f9fae852da2">BuyComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that a purchase transaction has been completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb796ef2-6d08-4746-952b-24ac51ae7733">ChangeView</a>
</td>
<td align="left" width="63%">
Changes the view in Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe8772fa-2eb4-4dfe-b677-e667b6021690">DownloadTrack</a>
</td>
<td align="left" width="63%">
Instructs Windows Media Player to download or not to download a particular media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e77785d1-71e3-474d-bad1-4b1145a06d01">GetCatalogVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version information for the online store catalog currently in use by Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8fbac82-77dc-4316-860d-cdf53e8bb9a7">GetContentIDsInLibrary</a>
</td>
<td align="left" width="63%">
Retrieves an array of content IDs that represent the music tracks in the library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e46a3378-a8e3-40c1-9cca-b6444286b3b5">ListContentsComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the content partner plug-in is finished adding content to a list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8402662-7e14-4be7-bc2d-45338bf2a226">Notify</a>
</td>
<td align="left" width="63%">
Provides notifications from the content partner plug-in to Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/426941d9-8d10-4c30-bf2d-cae3f48b51c6">RefreshLicenseComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a request to update the license for a media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa5c6b8f-5797-4703-9be8-e3c3a1f1f5f3">SendMessageComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93b2938c-e3e7-4c9f-92b1-a0b37ed573e6">ShowPopup</a>
</td>
<td align="left" width="63%">
Instructs Windows Media Player to display an HTML-based dialog box that hosts a webpage provided by the online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d21d9a0-1a7c-4f4e-9c9d-36a0d30ea63f">UpdateDeviceComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a call to <a href="https://msdn.microsoft.com/893beb65-048f-4496-88e6-b0e0b8db0205">IWMPContentPartner::UpdateDevice</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf99ead7-a50c-4638-9f4c-5c43a8d0a0be">VerifyPermissionComplete</a>
</td>
<td align="left" width="63%">
Notifies Windows Media Player that the online store has finished processing a call to <a href="https://msdn.microsoft.com/7ff45264-6e49-4953-bc0a-b3652aee965d">IWMPContentPartner::VerifyPermission</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e6f45a50-029e-4347-9b25-10e9e32a56eb">Reference for Type 1 Online Stores</a>
 

 

