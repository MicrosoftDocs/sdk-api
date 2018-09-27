---
UID: NN:wmp.IWMPLibrarySharingServices
title: IWMPLibrarySharingServices
author: windows-sdk-content
description: The IWMPLibrarySharingServices interface provides methods to manage library sharing.To use this interface, you must create a remoted instance of the Windows Media Player control.
old-location: wmp\iwmplibrarysharingservices.htm
tech.root: WMP
ms.assetid: 24cac18c-a3aa-4cd0-b5f7-025db2eed0b8
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPLibrarySharingServices, IWMPLibrarySharingServices interface [Windows Media Player], IWMPLibrarySharingServices interface [Windows Media Player],described, IWMPLibrarySharingServicesInterface, wmp.iwmplibrarysharingservices, wmp/IWMPLibrarySharingServices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPLibrarySharingServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPLibrarySharingServices interface


## -description



The <b>IWMPLibrarySharingServices</b> interface provides methods to manage library sharing.

To use this interface, you must create a remoted instance of the Windows Media Player control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPLibrarySharingServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPLibrarySharingServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPLibrarySharingServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc0a1396-5b43-43dd-9e0d-b5b3a8cf5cdd">isLibraryShared</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the user's library is shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd643869-9111-423e-9f9c-7147d1e3c7b8">isLibrarySharingEnabled</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the user has enabled library sharing in Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87c335ee-c9af-4182-a460-118c53308dad">showLibrarySharing</a>
</td>
<td align="left" width="63%">
Displays the Windows Media Player <b>Library Sharing</b> dialog box.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPLibrarySharingServices</b> interface by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer</a> interface.
	


## -see-also




<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

