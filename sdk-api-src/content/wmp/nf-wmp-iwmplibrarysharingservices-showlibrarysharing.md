---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

