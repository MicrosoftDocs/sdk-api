---
UID: NN:gpmgmt.IGPMCSECollection
title: IGPMCSECollection (gpmgmt.h)
description: The IGPMCSECollection interface contains methods that enable applications to query a collection of client-side extensions (CSEs) when you use the Group Policy Management Console (GPMC) interfaces.
helpviewer_keywords: ["GPMCSECollection","IGPMCSECollection","IGPMCSECollection interface [GPMC]","IGPMCSECollection interface [GPMC]","described","_win32_igpmcsecollection","gpmc.igpmcsecollection","gpmgmt/IGPMCSECollection"]
old-location: gpmc\igpmcsecollection.htm
tech.root: gpmc
ms.assetid: e32c1c39-b817-4db6-ad76-b2e66b54d79d
ms.date: 12/05/2018
ms.keywords: GPMCSECollection, IGPMCSECollection, IGPMCSECollection interface [GPMC], IGPMCSECollection interface [GPMC],described, _win32_igpmcsecollection, gpmc.igpmcsecollection, gpmgmt/IGPMCSECollection
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
 - IGPMCSECollection
 - gpmgmt/IGPMCSECollection
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
 - IGPMCSECollection
 - IGPMCSECollection.Count
 - IGPMCSECollection.get_Count
 - IGPMCSECollection.Item
 - IGPMCSECollection.get_Item
 - GPMCSECollection
---

# IGPMCSECollection interface


## -description

The 
<b>IGPMCSECollection</b> interface contains methods that enable applications to query a collection of client-side extensions (CSEs) when you use the Group Policy Management Console (GPMC) interfaces. To create a <b>GPMCSECollection</b> object, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getclientsideextensions">IGPM::GetClientSideExtensions</a> method.

## -inheritance

The <b>IGPMCSECollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMCSECollection</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmclientsideextension">IGPMClientSideExtension</a>
