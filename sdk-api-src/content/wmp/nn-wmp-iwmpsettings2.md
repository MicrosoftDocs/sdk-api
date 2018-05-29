---
UID: NN:wmp.IWMPSettings2
title: IWMPSettings2
author: windows-sdk-content
description: The IWMPSettings2 interface provides methods that supplement the IWMPSettings interface.
old-location: wmp\iwmpsettings2.htm
old-project: WMP
ms.assetid: 0fb0c7be-015e-4081-8467-c382e0858195
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPSettings2, IWMPSettings2 interface [Windows Media Player], IWMPSettings2 interface [Windows Media Player],described, IWMPSettings2Interface, wmp.iwmpsettings2, wmp/IWMPSettings2
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
-	IWMPSettings2
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPSettings2 interface


## -description



The <b>IWMPSettings2</b> interface provides methods that supplement the <b>IWMPSettings</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSettings2</b> interface inherits from <a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings</a>. <b>IWMPSettings2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSettings2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/890154b7-0aa8-475f-afe9-9ce71997a656">get_defaultAudioLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the locale identifier (LCID) of the default audio language.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07ca80a3-5175-4b1f-b83c-0df41a010cbf">get_mediaAccessRights</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the permissions currently granted for library access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/925a4c0b-d613-4248-a341-bfc51d02cb85">requestMediaAccessRights</a>
</td>
<td align="left" width="63%">
Requests a specified level of access to the library.

</td>
</tr>
</table> 


Retrieve a pointer to an <b>IWMPSettings2</b> interface by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings</a> interface.

	


## -see-also




<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

