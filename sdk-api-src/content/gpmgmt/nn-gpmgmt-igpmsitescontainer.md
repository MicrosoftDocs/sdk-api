---
UID: NN:gpmgmt.IGPMSitesContainer
title: IGPMSitesContainer (gpmgmt.h)
description: The IGPMSitesContainer interface provides the methods required to access the scope of management (SOM) objects that represent sites in a forest.
helpviewer_keywords: ["GPMSitesContainer","IGPMSitesContainer","IGPMSitesContainer interface [GPMC]","IGPMSitesContainer interface [GPMC]","described","_win32_igpmsitescontainer","gpmc.igpmsitescontainer","gpmgmt/IGPMSitesContainer"]
old-location: gpmc\igpmsitescontainer.htm
tech.root: gpmc
ms.assetid: e3fdfd44-9e90-4206-b7e9-97d4ed6eb8af
ms.date: 12/05/2018
ms.keywords: GPMSitesContainer, IGPMSitesContainer, IGPMSitesContainer interface [GPMC], IGPMSitesContainer interface [GPMC],described, _win32_igpmsitescontainer, gpmc.igpmsitescontainer, gpmgmt/IGPMSitesContainer
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
 - IGPMSitesContainer
 - gpmgmt/IGPMSitesContainer
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
 - IGPMSitesContainer
 - GPMSitesContainer
---

# IGPMSitesContainer interface


## -description

The 
<b>IGPMSitesContainer</b> interface provides the methods required to access the scope of management (SOM) objects that represent sites in a forest. The <b>GPMSitesContainer</b> object represents the forest-level container that contains the actual sites in a forest. To create a <b>GPMSitesContainer</b> object, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getsitescontainer">IGPM::GetSitesContainer</a> method.

## -inheritance

The <b>IGPMSitesContainer</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMSitesContainer</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>
