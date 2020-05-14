---
UID: NN:gpmgmt.IGPMStarterGPOBackupCollection
title: IGPMStarterGPOBackupCollection (gpmgmt.h)
description: The IGPMStarterGPOBackupCollection interface contains methods that enable applications to access a collection of GPMStarterGPOBackup objects when using the Group Policy Management Console (GPMC) interfaces.helpviewer_keywords: ["GPMStarterGPOBackupCollection","IGPMStarterGPOBackupCollection","IGPMStarterGPOBackupCollection interface [GPMC]","IGPMStarterGPOBackupCollection interface [GPMC]","described","gpmc.igpmstartergpobackupcollection","gpmgmt/IGPMStarterGPOBackupCollection"]
old-location: gpmc\igpmstartergpobackupcollection.htm
tech.root: gpmc
ms.assetid: df9f29d0-8636-4393-8f7e-c9e22f3692f5
ms.date: 12/05/2018
ms.keywords: GPMStarterGPOBackupCollection, IGPMStarterGPOBackupCollection, IGPMStarterGPOBackupCollection interface [GPMC], IGPMStarterGPOBackupCollection interface [GPMC],described, gpmc.igpmstartergpobackupcollection, gpmgmt/IGPMStarterGPOBackupCollection
f1_keywords:
- gpmgmt/IGPMStarterGPOBackupCollection
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
- IGPMStarterGPOBackupCollection
- IGPMStarterGPOBackupCollection.Count
- IGPMStarterGPOBackupCollection.get_Count
- IGPMStarterGPOBackupCollection.Item
- IGPMStarterGPOBackupCollection.get_Item
- GPMStarterGPOBackupCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMStarterGPOBackupCollection interface


## -description


The 
<b>IGPMStarterGPOBackupCollection</b> interface contains methods that enable applications to access a collection of 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">GPMStarterGPOBackup</a> objects when using the  Group Policy Management Console (GPMC) interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPOBackupCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMStarterGPOBackupCollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpobackupcollection-get__newenum">get__NewEnum</a>
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
Number of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMStarterGPOBackup</a> objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Item</b>

</td>
<td align="left" width="63%">
A specific <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMStarterGPOBackup</a> object from the collection.

</td>
</tr>
</table> 


## -remarks



For more information, see 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackupdirex-searchbackups">SearchBackups</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdirex">IGPMBackupDirEx</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMStarterGPOBackup</a>
 

 

