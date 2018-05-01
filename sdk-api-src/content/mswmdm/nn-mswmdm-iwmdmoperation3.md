---
UID: NN:mswmdm.IWMDMOperation3
title: IWMDMOperation3
author: windows-driver-content
description: The optional, application-implemented IWMDMOperation3 interface extends IWMDMOperation by providing a new method for transferring data unencrypted for added efficiency.
old-location: wmdm\iwmdmoperation3.htm
old-project: WMDM
ms.assetid: 5ab4fdd2-d0bf-4e2c-b529-331ffa4c8403
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IWMDMOperation3, IWMDMOperation3 interface [windows Media Device Manager], IWMDMOperation3 interface [windows Media Device Manager], described, IWMDMOperation3Interface, mswmdm/IWMDMOperation3, wmdm.iwmdmoperation3
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	IWMDMOperation3
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMOperation3 interface


## -description



The optional, application-implemented <b>IWMDMOperation3</b> interface extends <b>IWMDMOperation</b> by providing a new method for transferring data unencrypted for added efficiency.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMOperation3</b> interface inherits from <a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation</a>. <b>IWMDMOperation3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMOperation3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5cc0151-35c0-4de6-9bb3-f07339c60042">TransferObjectDataOnClearChannel</a>
</td>
<td align="left" width="63%">
Transfers a block of data to or from the device more efficiently than <a href="https://msdn.microsoft.com/ba3f29d9-88cd-4050-aa9f-f9317745a16b">IWMDMOperation::TransferObjectData</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/b3f7e92a-8feb-47cd-ae50-bc5bf9a37958">IWMDMOperation2 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

