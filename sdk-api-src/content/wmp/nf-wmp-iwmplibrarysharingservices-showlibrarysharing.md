---
UID: NF:wmp.IWMPLibrarySharingServices.showLibrarySharing
title: IWMPLibrarySharingServices::showLibrarySharing
author: windows-sdk-content
description: The showLibrarySharing method displays the Windows Media Player Library Sharing dialog box.
old-location: wmp\iwmplibrarysharingservices_showlibrarysharing.htm
old-project: WMP
ms.assetid: 87c335ee-c9af-4182-a460-118c53308dad
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPLibrarySharingServices interface [Windows Media Player],showLibrarySharing method, IWMPLibrarySharingServices.showLibrarySharing, IWMPLibrarySharingServices::showLibrarySharing, IWMPLibrarySharingServicesshowLibrarySharing, showLibrarySharing, showLibrarySharing method [Windows Media Player], showLibrarySharing method [Windows Media Player],IWMPLibrarySharingServices interface, wmp.iwmplibrarysharingservices_showlibrarysharing, wmp/IWMPLibrarySharingServices::showLibrarySharing
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPLibrarySharingServices.showLibrarySharing
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPLibrarySharingServices::showLibrarySharing


## -description



The <b>showLibrarySharing</b> method displays the Windows Media Player <b>Library Sharing</b> dialog box.




## -parameters






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



The <b>Library Sharing</b> dialog box enables the user to configure library sharing. Users can access this dialog box by pointing to <b>Tools</b>, then clicking <b>Options</b>, and then clicking <b>Configure Media Sharing</b> in the Windows Media Player menu; or by clicking the arrow below the <b>Library</b> tab and then clicking <b>Library Sharing</b>.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/24cac18c-a3aa-4cd0-b5f7-025db2eed0b8">IWMPLibrarySharingServices Interface</a>
 

 

