---
UID: NN:contentpartner.IWMPContentPartner
title: IWMPContentPartner
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartner.htm
old-project: WMP
ms.assetid: 2078ebd4-3570-4c39-9081-1b55d9e8286f
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPContentPartner, IWMPContentPartner interface [Windows Media Player], IWMPContentPartner interface [Windows Media Player],described, IWMPContentPartnerInterface, contentpartner/IWMPContentPartner, wmp.iwmpcontentpartner
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WMPTransactionType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	contentpartner.h
api_name:
-	IWMPContentPartner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentPartner interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentPartner</b> interface provides methods that Windows Media Player calls to integrate its user interface with an online store's catalog and services. This interface is implemented by a content partner plug-in, which is provided by the online store.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPContentPartner</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPContentPartner</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0fb3a94d-8c8e-4d04-b9ca-56ad2e066aac">Authenticate</a>
</td>
<td align="left" width="63%">
Initiates an attempt to authenticate the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a79c3d6e-b587-4bbc-b3bf-6489a54d71f9">Buy</a>
</td>
<td align="left" width="63%">
Initiates the purchase of digital media content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1faec369-199e-48d4-9c0a-6cbad39a7073">CanBuySilent</a>
</td>
<td align="left" width="63%">
Calculates the total price of a purchase and determines whether the purchase can proceed without displaying a dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4febe7ce-1aa1-4738-a4cc-353f81ca649e">CompareContainerListPrices</a>
</td>
<td align="left" width="63%">
Compares the price of two content container lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fa3ed40-e155-4e42-b031-d6cb8f8b4ac4">Download</a>
</td>
<td align="left" width="63%">
Initiates the download of a set of media items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9614e266-259c-411f-93cf-9be87c930b16">DownloadTrackComplete</a>
</td>
<td align="left" width="63%">
Notifies the content partner plug-in that Windows Media Player has finished downloading a track or that the download attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/291440d5-b6d3-4586-98d2-3f7c56da29aa">GetCatalogURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL from which to retrieve an update to the online store's current catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc6dfd97-50bb-438c-9cd6-3eac91e99cab">GetCommands</a>
</td>
<td align="left" width="63%">
Retrieves context menu commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca63b65c-9a60-4c5d-a9f2-69d1168c53a5">GetContentPartnerInfo</a>
</td>
<td align="left" width="63%">
Retrieves specific information about the online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7355c45-fb58-45f4-b7e4-3dd2c3f8c918">GetItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves information (for example, a URL or a caption) related to an item owned by an online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a48935ea-8275-4b68-a1ab-006a23c455ad">GetListContents</a>
</td>
<td align="left" width="63%">
Initiates the retrieval of a dynamic list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b9c25bc-35f7-429a-b465-45e166e2ed1a">GetStreamingURL</a>
</td>
<td align="left" width="63%">
Retrieves the streaming URL of a track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bfe7d84-9f65-4bd4-867a-65c96291397d">GetTemplate</a>
</td>
<td align="left" width="63%">
Retrieves the URL of the discovery page to be displayed when the library view changes in Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee46a7c2-2d5b-4c7f-954e-cad6011afc78">InvokeCommand</a>
</td>
<td align="left" width="63%">
Invokes a context menu command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn915474">Login</a>
</td>
<td align="left" width="63%">
Logs the user in to the online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8919dd66-1ec0-4551-8132-7067957bb545">Logout</a>
</td>
<td align="left" width="63%">
Ends the user's online store session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9464ce82-cd84-4a35-83d2-e46198c0c1e7">Notify</a>
</td>
<td align="left" width="63%">
Provides the content partner plug-in with event notifications from Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f0d8ed9-027c-45a3-a61a-f6d571e78a0a">RefreshLicense</a>
</td>
<td align="left" width="63%">
Initiates the update of a license for the specified media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a>
</td>
<td align="left" width="63%">
Enables discovery pages to send messages to the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb3b0c68-b071-476c-ab14-e4ee34bc9044">SetCallback</a>
</td>
<td align="left" width="63%">
Provides the plug-in with a pointer for calling Windows Media Player methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0505a1e9-489f-416a-88b8-e8b76ae94b70">StationEvent</a>
</td>
<td align="left" width="63%">
Notifies the plug-in of events during playback of a Windows Media metafile playlist (ASX).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/893beb65-048f-4496-88e6-b0e0b8db0205">UpdateDevice</a>
</td>
<td align="left" width="63%">
Notifies the content-partner plug-in that a portable device is being synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ff45264-6e49-4953-bc0a-b3652aee965d">VerifyPermission</a>
</td>
<td align="left" width="63%">
Initiates the process of verifying permission for Windows Media Player to perform an action.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e6f45a50-029e-4347-9b25-10e9e32a56eb">Reference for Type 1 Online Stores</a>
 

 

