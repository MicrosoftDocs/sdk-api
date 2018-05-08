---
UID: NN:mswmdm.IWMDMProgress
title: IWMDMProgress
author: windows-driver-content
description: The optional, application-implemented IWMDMProgress allows an application to track the progress of operations, such as formatting media or file transfers.
old-location: wmdm\iwmdmprogress.htm
old-project: WMDM
ms.assetid: 9af022a6-19b4-41b7-b951-0acad6aab4a2
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IWMDMProgress, IWMDMProgress interface [windows Media Device Manager], IWMDMProgress interface [windows Media Device Manager],described, IWMDMProgressInterface, mswmdm/IWMDMProgress, wmdm.iwmdmprogress
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
-	IWMDMProgress
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMProgress interface


## -description



The optional, application-implemented <b>IWMDMProgress</b> allows an application to track the progress of operations, such as formatting media or file transfers. This interface is submitted to, and called by, the <a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals</a> and <a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl</a> interfaces.

These methods do not provide a way for the application to know which operation is being tracked. However, the <b>IWMDMProgress3</b> methods do provide a means to identify the operation; if possible, you should implement that interface instead.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMProgress</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/207b7cb5-4471-4be9-8252-9d467d67d7a2">Begin</a>
</td>
<td align="left" width="63%">
Indicates that an operation is beginning. An estimate of the duration of the operation is provided when possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0edddd8c-8144-40dc-801c-eb8c899be249">End</a>
</td>
<td align="left" width="63%">
Indicates that an operation is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e85b6b46-2c42-461f-90b5-71b48bc4a111">Progress</a>
</td>
<td align="left" width="63%">
Indicates that an operation is still in progress.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b4fc7714-a7d0-409f-a47c-4903bab883cc">Enabling Notifications</a>



<a href="https://msdn.microsoft.com/59619571-0ab7-42a4-ad25-c420ec9667a3">IWMDMProgress2 Interface</a>



<a href="https://msdn.microsoft.com/fc3a7031-ac1b-45cf-889b-2d40d50b347d">IWMDMProgress3 Interface</a>



<a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl Interface</a>



<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

