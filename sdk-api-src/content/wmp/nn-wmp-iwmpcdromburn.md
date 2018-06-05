---
UID: NN:wmp.IWMPCdromBurn
title: IWMPCdromBurn
author: windows-sdk-content
description: The IWMPCdromBurn interface provides methods to manage creating audio CDs.
old-location: wmp\iwmpcdromburn.htm
old-project: WMP
ms.assetid: 45116a33-62f9-4c7d-b246-25905cbaf118
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPCdromBurn, IWMPCdromBurn interface [Windows Media Player], IWMPCdromBurn interface [Windows Media Player],described, IWMPCdromBurnInterface, wmp.iwmpcdromburn, wmp/IWMPCdromBurn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmp.h
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.h
api_name:
-	IWMPCdromBurn
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCdromBurn interface


## -description



The <b>IWMPCdromBurn</b> interface provides methods to manage creating audio CDs.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPCdromBurn</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPCdromBurn</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPCdromBurn</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93a37f59-4269-4f84-93dc-8350aabd4ebe">erase</a>
</td>
<td align="left" width="63%">
Erases the current CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/564a3978-555e-4cbc-90fe-b29f61349260">get_burnFormat</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates the type of CD to burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b31f4e87-2029-4001-94c7-268b14807cf0">get_burnPlaylist</a>
</td>
<td align="left" width="63%">
Retrieves the current playlist to burn to the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4941e1be-1ed2-4d8e-ad16-79ddbdcd71bf">get_burnProgress</a>
</td>
<td align="left" width="63%">
Retrieves the CD burning progress as percent complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6bcb8d6-07ad-4d8f-a94a-6b8c1b7f0c2b">get_burnState</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration value that indicates the current burn state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89197e65-036c-4ffb-8b08-4ab8c194f92f">get_label</a>
</td>
<td align="left" width="63%">
Retrieves the CD volume label string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f54b406f-0441-4ed3-8f8b-6794ab2180d9">getItemInfo</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified attribute for the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11876b73-10a1-49e2-ad45-33d9641c3647">isAvailable</a>
</td>
<td align="left" width="63%">
Provides information about the CD drive and media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1352e2f6-cad8-4d86-b973-b7d4d8f0c448">put_burnFormat</a>
</td>
<td align="left" width="63%">
Specifies the type of CD to burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26fad65c-d371-4e7c-a86e-1ddb24175909">put_burnPlaylist</a>
</td>
<td align="left" width="63%">
Specifies the playlist to burn to CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84407961-5d79-4845-a81a-283b3689e562">put_label</a>
</td>
<td align="left" width="63%">
Specifies the label string for the CD volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a1ca071-0a61-4ef5-b8c1-18336cf5b1b0">refreshStatus</a>
</td>
<td align="left" width="63%">
Updates the status information for the current burn playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35357dca-4093-4c83-9cc9-f0dee1241e76">startBurn</a>
</td>
<td align="left" width="63%">
Burns the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf001a08-97e9-4f88-919a-54651e3bfd5d">stopBurn</a>
</td>
<td align="left" width="63%">
Stops the CD burning process.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

