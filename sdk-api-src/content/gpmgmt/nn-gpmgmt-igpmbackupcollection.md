---
UID: NN:gpmgmt.IGPMBackupCollection
title: IGPMBackupCollection (gpmgmt.h)
description: The IGPMBackupCollection interface contains methods that enable applications to access a collection of GPMBackup objects when using the Group Policy Management Console (GPMC) interfaces.helpviewer_keywords: ["GPMBackupCollection","IGPMBackupCollection","IGPMBackupCollection interface [GPMC]","IGPMBackupCollection interface [GPMC]","described","_win32_igpmbackupcollection","gpmc.igpmbackupcollection","gpmgmt/IGPMBackupCollection"]
old-location: gpmc\igpmbackupcollection.htm
tech.root: gpmc
ms.assetid: cd9e6b58-6fbc-449a-9941-b33761797199
ms.date: 12/05/2018
ms.keywords: GPMBackupCollection, IGPMBackupCollection, IGPMBackupCollection interface [GPMC], IGPMBackupCollection interface [GPMC],described, _win32_igpmbackupcollection, gpmc.igpmbackupcollection, gpmgmt/IGPMBackupCollection
f1_keywords:
- gpmgmt/IGPMBackupCollection
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMBackupCollection interface


## -description


The 
<b>IGPMBackupCollection</b> interface contains methods that enable applications to access a collection of 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> objects when using the  Group Policy Management Console (GPMC) interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackupCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMBackupCollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackupcollection-get__newenum">get__NewEnum</a>
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackupdir-searchbackups">SearchBackups Method of the IGMPBackupDirInterface</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">IGPMBackupDir</a>
 

 

