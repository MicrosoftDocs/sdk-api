---
UID: NN:gpmgmt.IGPMBackupCollection
title: IGPMBackupCollection
author: windows-sdk-content
description: The IGPMBackupCollection interface contains methods that enable applications to access a collection of GPMBackup objects when using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmbackupcollection.htm
tech.root: GPMC
ms.assetid: cd9e6b58-6fbc-449a-9941-b33761797199
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GPMBackupCollection, IGPMBackupCollection, IGPMBackupCollection interface [GPMC], IGPMBackupCollection interface [GPMC],described, _win32_igpmbackupcollection, gpmc.igpmbackupcollection, gpmgmt/IGPMBackupCollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMBackupCollection
 - IGPMBackupCollection.Count
 - IGPMBackupCollection.get_Count
 - IGPMBackupCollection.Item
 - IGPMBackupCollection.get_Item
 - GPMBackupCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMBackupCollection interface


## -description


The 
<b>IGPMBackupCollection</b> interface contains methods that enable applications to access a collection of 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> objects when using the  Group Policy Management Console (GPMC) interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackupCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMBackupCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMBackupCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cad0ead4-cfd4-450e-95f3-9a52774b6c0e">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an interface on an enumerator object for the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackupCollection</b> interface has these properties.
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
Number of GPMBackup objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Item</b>

</td>
<td align="left" width="63%">
A specific GPMBackup object from the collection.

</td>
</tr>
</table> 


## -remarks



For more information, see 
<a href="https://msdn.microsoft.com/71e1991f-c24f-43fe-8f3e-83f5b02cec6b">SearchBackups Method of the IGMPBackupDirInterface</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">IGPMBackupDir</a>
 

 

