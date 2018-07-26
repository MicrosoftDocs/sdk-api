---
UID: NN:wuapi.IAutomaticUpdates2
title: IAutomaticUpdates2
author: windows-sdk-content
description: Contains the functionality of Automatic Updates.
old-location: wua\iautomaticupdates2.htm
old-project: wua_sdk
ms.assetid: 9cb09bb2-5532-446b-9441-0987d50c6228
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IAutomaticUpdates2, IAutomaticUpdates2 interface [Windows Update Agent], IAutomaticUpdates2 interface [Windows Update Agent],described, wua.iautomaticupdates2, wuapi/IAutomaticUpdates2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IAutomaticUpdates2
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IAutomaticUpdates2 interface


## -description


Contains the functionality of Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdates2</b> interface inherits from <a href="https://msdn.microsoft.com/b5f05e2a-ad60-4d4c-8bdd-1c03df3d508d">IAutomaticUpdates</a>. <b>IAutomaticUpdates2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAutomaticUpdates2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b83f6833-5318-42ca-a1d6-30b6590873bb">Results</a>
</td>
<td align="left" width="63%">
Returns a pointer to an 
     <a href="https://msdn.microsoft.com/fe9a5ea3-9d59-450b-8c5e-3444ec13dc97">IAutomaticUpdatesResults</a> interface.

</td>
</tr>
</table> 


## -remarks



You can create a new instance of this interface by using the AutomaticUpdates coclass. Use the 
    Microsoft.Update.AutoUpdate program identifier to create the object.




## -see-also




<a href="https://msdn.microsoft.com/b5f05e2a-ad60-4d4c-8bdd-1c03df3d508d">IAutomaticUpdates</a>
 

 

