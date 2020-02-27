---
UID: NN:gpmgmt.IGPM2
title: IGPM2 (gpmgmt.h)
description: The IGPM2 interface extends the GPMBackupDir and InitializeReporting methods of the IGPM interface of the Group Policy Management Console (GPMC).
old-location: gpmc\igpm2.htm
tech.root: gpmc
ms.assetid: f9cd432a-3974-4fc4-9e32-1d8e2df1601c
ms.date: 12/05/2018
ms.keywords: IGPM2, IGPM2 interface [GPMC], IGPM2 interface [GPMC],described, gpmc.igpm2, gpmgmt/IGPM2
f1_keywords:
- gpmgmt/IGPM2
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
- IGPM2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPM2 interface


## -description


The 
<b>IGPM2</b> interface extends the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">GPMBackupDir</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-initializereporting">InitializeReporting</a> methods of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a> interface of the Group Policy Management Console (GPMC).

The <b>GPM</b> object is the only object used with 
the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPM2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>. <b>IGPM2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGPM2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm2-getbackupdirex">GetBackupDirEx</a>
</td>
<td align="left" width="63%">
Creates and returns a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">GPMBackupDir</a> object which you can use to access 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> and  
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">GPMBackupCollection</a> objects or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">GPMStarterGPOBackup</a> and  
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackupcollection">GPMStarterGPOBackupCollection</a> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm2-initializereportingex">InitializeReportingEx</a>
</td>
<td align="left" width="63%">
Sets the location of the .adm files specified by user and initiates reporting with options.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/gpmc-interfaces">GPMC Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>
 

 

