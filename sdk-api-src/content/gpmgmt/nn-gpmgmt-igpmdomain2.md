---
UID: NN:gpmgmt.IGPMDomain2
title: IGPMDomain2 (gpmgmt.h)
description: Represents a given domain and supports methods that allow you to query scope of management (SOM) objects, create, restore and query Starter GPOs, and create and query WMI filters when you are using the Group Policy Management Console (GPMC) interfaces.
helpviewer_keywords: ["IGPMDomain2","IGPMDomain2 interface [GPMC]","IGPMDomain2 interface [GPMC]","described","gpmc.igpmdomain2","gpmgmt/IGPMDomain2"]
old-location: gpmc\igpmdomain2.htm
tech.root: gpmc
ms.assetid: 5abfea14-0cb9-46ea-915c-93a8d8b2477b
ms.date: 12/05/2018
ms.keywords: IGPMDomain2, IGPMDomain2 interface [GPMC], IGPMDomain2 interface [GPMC],described, gpmc.igpmdomain2, gpmgmt/IGPMDomain2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMDomain2
 - gpmgmt/IGPMDomain2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMDomain2
---

# IGPMDomain2 interface


## -description

The 
<b>IGPMDomain2</b> interface represents a specified domain and supports certain methods.

These methods allow you to perform the following tasks when you are using the Group Policy Management Console (GPMC) interfaces:
<ul>
<li>Query scope of management (SOM) objects</li>
<li>Create, restore, and query Starter Group Policy objects (GPOs)</li>
<li>Create and query Windows Management Instrumentation (WMI) filters</li>
</ul>To create a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">GPMDomain</a> object, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getdomain">IGPM::GetDomain</a> method.

## -inheritance

The <b>IGPMDomain2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>. <b>IGPMDomain2</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm2">IGPM2</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">IGPMStarterGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">IGPMStarterGPOBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpocollection">IGPMStarterGPOCollection</a>
