---
UID: NN:wmp.IWMPLibraryServices
title: IWMPLibraryServices
author: windows-sdk-content
description: The IWMPLibraryServices interface provides methods to enumerate libraries.
old-location: wmp\iwmplibraryservices.htm
old-project: WMP
ms.assetid: 9ed6d02e-15ca-425f-8642-e32a5adfaa55
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPLibraryServices, IWMPLibraryServices interface [Windows Media Player], IWMPLibraryServices interface [Windows Media Player],described, IWMPLibraryServicesInterface, wmp.iwmplibraryservices, wmp/IWMPLibraryServices
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.h
api_name:
-	IWMPLibraryServices
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPLibraryServices interface


## -description



The <b>IWMPLibraryServices</b> interface provides methods to enumerate libraries.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPLibraryServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPLibraryServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPLibraryServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e592fc2e-97d8-4d3c-bbef-7cbaa63a6909">getCountByType</a>
</td>
<td align="left" width="63%">
Retrieves the count of available libraries of a specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/766cfd4e-53e6-44a8-87e6-2b9c1fa2ff3f">getLibraryByType</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPLibrary</b> interface that represents the library that has the specified type and index.

</td>
</tr>
</table> 


Retrieve a pointer to <b>IWMPLibraryServices</b> by calling <b>QueryInterface</b> through <a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer</a> from a local or remoted Windows Media Player ActiveX control.
	
	


## -see-also




<a href="https://msdn.microsoft.com/add0ed43-d83f-4793-b1f6-ccad0f01854c">IWMPLibrary Interface</a>



<a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

