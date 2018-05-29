---
UID: NN:shobjidl_core.IUpdateIDList
title: IUpdateIDList
author: windows-sdk-content
description: Provides a method to update the ITEMIDLIST of the child of an folder object.
old-location: shell\IUpdateIDList.htm
old-project: shell
ms.assetid: e6d94975-de33-497e-95a9-b89e8f8f0134
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUpdateIDList, IUpdateIDList interface [Windows Shell], IUpdateIDList interface [Windows Shell],described, _shell_IUpdateIDList, shell.IUpdateIDList, shobjidl_core/IUpdateIDList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IUpdateIDList
product: Windows
targetos: Windows
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IUpdateIDList interface


## -description


Provides a method to update the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> of the child of an folder object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateIDList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUpdateIDList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUpdateIDList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Updates the provided child <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> based on the parameters specified by the provided <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement this interface for an <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> implementation to update the provided child <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.



