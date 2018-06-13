---
UID: NN:gpmgmt.IGPMStarterGPOBackupCollection
title: IGPMStarterGPOBackupCollection
author: windows-sdk-content
description: The IGPMStarterGPOBackupCollection interface contains methods that enable applications to access a collection of GPMStarterGPOBackup objects when using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmstartergpobackupcollection.htm
old-project: GPMC
ms.assetid: df9f29d0-8636-4393-8f7e-c9e22f3692f5
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GPMStarterGPOBackupCollection, IGPMStarterGPOBackupCollection, IGPMStarterGPOBackupCollection interface [GPMC], IGPMStarterGPOBackupCollection interface [GPMC],described, gpmc.igpmstartergpobackupcollection, gpmgmt/IGPMStarterGPOBackupCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMStarterGPOBackupCollection
 - IGPMStarterGPOBackupCollection.Count
 - IGPMStarterGPOBackupCollection.get_Count
 - IGPMStarterGPOBackupCollection.Item
 - IGPMStarterGPOBackupCollection.get_Item
 - GPMStarterGPOBackupCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMStarterGPOBackupCollection interface


## -description


The 
<b>IGPMStarterGPOBackupCollection</b> interface contains methods that enable applications to access a collection of 
<a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">GPMStarterGPOBackup</a> objects when using the  Group Policy Management Console (GPMC) interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPOBackupCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGPMStarterGPOBackupCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMStarterGPOBackupCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87748dba-fe77-43a5-a9d1-8e068b96e197">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an interface on an enumerator object for the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPOBackupCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Count</b>

</td>
<td align="left" width="63%">
Number of <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMStarterGPOBackup</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Item</b>

</td>
<td align="left" width="63%">
A specific <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMStarterGPOBackup</a> object from the collection.

</td>
</tr>
</table> 


## -remarks



For more information, see 
<a href="https://msdn.microsoft.com/e45f012e-ce88-4baf-88a2-bd61e365b291">SearchBackups</a>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/3008e70c-cc34-45b0-bdfc-17f2e9cd5de0">IGPMBackupDirEx</a>



<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMStarterGPOBackup</a>
 

 

