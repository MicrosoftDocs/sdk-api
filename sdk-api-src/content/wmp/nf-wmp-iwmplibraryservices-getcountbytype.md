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

# IWMPLibraryServices::getCountByType


## -description



The <b>getCountByType</b> method retrieves the count of available libraries of a specified type.




## -parameters




### -param wmplt [in]


<a href="https://msdn.microsoft.com/bf0e7140-5a33-4841-bd55-ac07dae09c41">WMPLibraryType</a> enumeration value that specifies the type of library to count.


### -param plCount [out]

Pointer to a <b>long</b> that receives the library count.


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



To obtain a count of the libraries represented by the wmpltRemote value of the <b>WMPLibraryType</b> enumeration, the Player control must be running in remote mode. For information about running the Player control in remote mode, see <a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>.

You must initialize the <i>plCount</i> variable before passing in its pointer.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/9ed6d02e-15ca-425f-8642-e32a5adfaa55">IWMPLibraryServices Interface</a>



<a href="https://msdn.microsoft.com/bf0e7140-5a33-4841-bd55-ac07dae09c41">WMPLibraryType</a>
 

 

