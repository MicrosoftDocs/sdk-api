---
UID: NN:mswmdm.IWMDMStorageControl3
title: IWMDMStorageControl3
author: windows-sdk-content
description: The IWMDMStorageControl3 interface extends IWMDMStorageControl2 by providing an Insert method that accepts an IWMDMMetaData interface pointer.
old-location: wmdm\iwmdmstoragecontrol3.htm
old-project: WMDM
ms.assetid: bc5165c2-791d-4549-a271-78728625b219
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWMDMStorageControl3, IWMDMStorageControl3 interface [windows Media Device Manager], IWMDMStorageControl3 interface [windows Media Device Manager],described, IWMDMStorageControl3Interface, mswmdm/IWMDMStorageControl3, wmdm.iwmdmstoragecontrol3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mswmdm.h
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	IWMDMStorageControl3
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorageControl3 interface


## -description



The <b>IWMDMStorageControl3</b> interface extends <b>IWMDMStorageControl2</b> by providing an <b>Insert</b> method that accepts an <a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData</a> interface pointer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorageControl3</b> interface inherits from <a href="https://msdn.microsoft.com/c5a17642-5253-4d01-895a-09d00284f341">IWMDMStorageControl2</a>. <b>IWMDMStorageControl3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorageControl3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/044a6571-8ec0-48af-b105-07c60c25d68a">Insert3</a>
</td>
<td align="left" width="63%">
Puts content into/next to the storage. Extends <a href="https://msdn.microsoft.com/bc6cc03c-e13a-45d8-afcb-1fadd5f4dd8e">IWMDMStorageControl2::Insert2</a> method by allowing the application to pass in an <b>IWMDMMetaData</b> interface pointer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl Interface</a>



<a href="https://msdn.microsoft.com/c5a17642-5253-4d01-895a-09d00284f341">IWMDMStorageControl2 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

