---
UID: NN:contentpartner.IWMPContentPartner
title: IWMPContentPartner
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartner.htm
tech.root: WMP
ms.assetid: 2078ebd4-3570-4c39-9081-1b55d9e8286f
ms.author: windowssdkdev
ms.date: 08/30/2018
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPContentPartner interface


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentPartner</b> interface provides methods that Windows Media Player calls to integrate its user interface with an online store's catalog and services. This interface is implemented by a content partner plug-in, which is provided by the online store.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPContentPartner</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IWMPContentPartner</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563156(v=VS.85).aspx">Authenticate</a>
</td>
<td align="left" width="63%">
Initiates an attempt to authenticate the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563157(v=VS.85).aspx">Buy</a>
</td>
<td align="left" width="63%">
Initiates the purchase of digital media content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563158(v=VS.85).aspx">CanBuySilent</a>
</td>
<td align="left" width="63%">
Calculates the total price of a purchase and determines whether the purchase can proceed without displaying a dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563159(v=VS.85).aspx">CompareContainerListPrices</a>
</td>
<td align="left" width="63%">
Compares the price of two content container lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563160(v=VS.85).aspx">Download</a>
</td>
<td align="left" width="63%">
Initiates the download of a set of media items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563161(v=VS.85).aspx">DownloadTrackComplete</a>
</td>
<td align="left" width="63%">
Notifies the content partner plug-in that Windows Media Player has finished downloading a track or that the download attempt failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563162(v=VS.85).aspx">GetCatalogURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL from which to retrieve an update to the online store's current catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563163(v=VS.85).aspx">GetCommands</a>
</td>
<td align="left" width="63%">
Retrieves context menu commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563164(v=VS.85).aspx">GetContentPartnerInfo</a>
</td>
<td align="left" width="63%">
Retrieves specific information about the online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563165(v=VS.85).aspx">GetItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves information (for example, a URL or a caption) related to an item owned by an online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563166(v=VS.85).aspx">GetListContents</a>
</td>
<td align="left" width="63%">
Initiates the retrieval of a dynamic list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563167(v=VS.85).aspx">GetStreamingURL</a>
</td>
<td align="left" width="63%">
Retrieves the streaming URL of a track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563168(v=VS.85).aspx">GetTemplate</a>
</td>
<td align="left" width="63%">
Retrieves the URL of the discovery page to be displayed when the library view changes in Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563169(v=VS.85).aspx">InvokeCommand</a>
</td>
<td align="left" width="63%">
Invokes a context menu command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563170(v=VS.85).aspx">Login</a>
</td>
<td align="left" width="63%">
Logs the user in to the online store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563171(v=VS.85).aspx">Logout</a>
</td>
<td align="left" width="63%">
Ends the user's online store session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563172(v=VS.85).aspx">Notify</a>
</td>
<td align="left" width="63%">
Provides the content partner plug-in with event notifications from Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563173(v=VS.85).aspx">RefreshLicense</a>
</td>
<td align="left" width="63%">
Initiates the update of a license for the specified media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563174(v=VS.85).aspx">SendMessage</a>
</td>
<td align="left" width="63%">
Enables discovery pages to send messages to the plug-in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563175(v=VS.85).aspx">SetCallback</a>
</td>
<td align="left" width="63%">
Provides the plug-in with a pointer for calling Windows Media Player methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563176(v=VS.85).aspx">StationEvent</a>
</td>
<td align="left" width="63%">
Notifies the plug-in of events during playback of a Windows Media metafile playlist (ASX).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563177(v=VS.85).aspx">UpdateDevice</a>
</td>
<td align="left" width="63%">
Notifies the content-partner plug-in that a portable device is being synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563178(v=VS.85).aspx">VerifyPermission</a>
</td>
<td align="left" width="63%">
Initiates the process of verifying permission for Windows Media Player to perform an action.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd564243(v=VS.85).aspx">Reference for Type 1 Online Stores</a>
 

 

