---
UID: NN:gpmgmt.IGPMStarterGPOCollection
title: IGPMStarterGPOCollection (gpmgmt.h)
description: The IGPMStarterGPOCollection interface contains methods that enable applications to access a collection of Group Policy Objects (GPOs) when using the Group Policy Management Console (GPMC) interfaces.
helpviewer_keywords: ["GPMStarterGPOCollection","IGPMStarterGPOCollection","IGPMStarterGPOCollection interface [GPMC]","IGPMStarterGPOCollection interface [GPMC]","described","gpmc.igpmstartergpocollection","gpmgmt/IGPMStarterGPOCollection"]
old-location: gpmc\igpmstartergpocollection.htm
tech.root: gpmc
ms.assetid: b650b1c6-0597-468a-afdc-a21d61f1a8a0
ms.date: 12/05/2018
ms.keywords: GPMStarterGPOCollection, IGPMStarterGPOCollection, IGPMStarterGPOCollection interface [GPMC], IGPMStarterGPOCollection interface [GPMC],described, gpmc.igpmstartergpocollection, gpmgmt/IGPMStarterGPOCollection
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
 - IGPMStarterGPOCollection
 - gpmgmt/IGPMStarterGPOCollection
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
 - IGPMStarterGPOCollection
 - IGPMStarterGPOCollection.Count
 - IGPMStarterGPOCollection.get_Count
 - IGPMStarterGPOCollection.Item
 - IGPMStarterGPOCollection.get_Item
 - GPMStarterGPOCollection
---

# IGPMStarterGPOCollection interface


## -description

The 
<b>IGPMStarterGPOCollection</b> interface contains methods that enable applications to access a collection of Group Policy Objects (GPOs) when using the Group Policy Management Console (GPMC) interfaces. You can obtain a <b>GPMStarterGPOCollection</b> object by calling the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-searchgpos">IGPMDomain2::SearchStarterGPOs</a> method.

## -inheritance

The <b>IGPMStarterGPOCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMStarterGPOCollection</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMStarterGPO</a>
