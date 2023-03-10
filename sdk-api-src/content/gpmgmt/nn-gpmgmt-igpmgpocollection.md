---
UID: NN:gpmgmt.IGPMGPOCollection
title: IGPMGPOCollection (gpmgmt.h)
description: The IGPMGPOCollection interface contains methods that enable applications to access a collection of Group Policy Objects (GPOs) when using the Group Policy Management Console (GPMC) interfaces.
helpviewer_keywords: ["GPMGPOCollection","IGPMGPOCollection","IGPMGPOCollection interface [GPMC]","IGPMGPOCollection interface [GPMC]","described","_win32_igpmgpocollection","gpmc.igpmgpocollection","gpmgmt/IGPMGPOCollection"]
old-location: gpmc\igpmgpocollection.htm
tech.root: gpmc
ms.assetid: 847aea86-48e9-428e-ae4d-e6a7e1e13428
ms.date: 12/05/2018
ms.keywords: GPMGPOCollection, IGPMGPOCollection, IGPMGPOCollection interface [GPMC], IGPMGPOCollection interface [GPMC],described, _win32_igpmgpocollection, gpmc.igpmgpocollection, gpmgmt/IGPMGPOCollection
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
 - IGPMGPOCollection
 - gpmgmt/IGPMGPOCollection
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
 - IGPMGPOCollection
 - IGPMGPOCollection.Count
 - IGPMGPOCollection.get_Count
 - IGPMGPOCollection.Item
 - IGPMGPOCollection.get_Item
 - GPMGPOCollection
---

# IGPMGPOCollection interface


## -description

The 
<b>IGPMGPOCollection</b> interface contains methods that enable applications to access a collection of Group Policy Objects (GPOs) when using the Group Policy Management Console (GPMC) interfaces. You can obtain a <b>GPMGPOCollection</b> object by calling the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-searchgpos">IGPMDomain::SearchGPOs</a> method.

## -inheritance

The <b>IGPMGPOCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMGPOCollection</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>
