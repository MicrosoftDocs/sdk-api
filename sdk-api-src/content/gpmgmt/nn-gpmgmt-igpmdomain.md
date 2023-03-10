---
UID: NN:gpmgmt.IGPMDomain
title: IGPMDomain (gpmgmt.h)
description: Represents a given domain and supports methods that allow you to query scope of management (SOM) objects, create, restore and query GPOs, and create and query WMI filters when you are using the Group Policy Management Console (GPMC) interfaces.
helpviewer_keywords: ["GPMDomain","IGPMDomain","IGPMDomain interface [GPMC]","IGPMDomain interface [GPMC]","described","_win32_igpmdomain","gpmc.igpmdomain","gpmgmt/IGPMDomain"]
old-location: gpmc\igpmdomain.htm
tech.root: gpmc
ms.assetid: c3639f07-7c8c-4440-ade4-b58abd2586d6
ms.date: 12/05/2018
ms.keywords: GPMDomain, IGPMDomain, IGPMDomain interface [GPMC], IGPMDomain interface [GPMC],described, _win32_igpmdomain, gpmc.igpmdomain, gpmgmt/IGPMDomain
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
 - IGPMDomain
 - gpmgmt/IGPMDomain
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
 - IGPMDomain
 - GPMDomain
---

# IGPMDomain interface


## -description

The 
<b>IGPMDomain</b> interface represents a specific domain and supports methods that allow you to perform the following tasks when you are using the Group Policy Management Console (GPMC) interfaces:
<ul>
<li>Query scope of management (SOM) objects.</li>
<li>Create, restore and query Group Policy objects (GPOs).</li>
<li>Create and query Windows Management Instrumentation (WMI) filters.</li>
</ul>To create a <b>GPMDomain</b> object, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getdomain">IGPM::GetDomain</a> method.

## -inheritance

The <b>IGPMDomain</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMDomain</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMGPOCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">IGPMSOM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsomcollection">IGPMSOMCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">IGPMWMIFilterCollection</a>
