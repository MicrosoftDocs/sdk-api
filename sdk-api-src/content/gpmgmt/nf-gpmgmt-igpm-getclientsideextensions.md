---
UID: NF:gpmgmt.IGPM.GetClientSideExtensions
title: IGPM::GetClientSideExtensions (gpmgmt.h)
description: Creates and returns a GPMCSECollection object that allows you to enumerate Group Policy client-side extensions (CSEs) that are registered on the local computer.
helpviewer_keywords: ["GPM object [GPMC]","GetClientSideExtensions method","GetClientSideExtensions","GetClientSideExtensions method [GPMC]","GetClientSideExtensions method [GPMC]","GPM object","GetClientSideExtensions method [GPMC]","IGPM interface","IGPM interface [GPMC]","GetClientSideExtensions method","IGPM.GetClientSideExtensions","IGPM::GetClientSideExtensions","_win32_igpm_getclientsideextensions","gpmc.igpm_getclientsideextensions","gpmgmt/IGPM::GetClientSideExtensions"]
old-location: gpmc\igpm_getclientsideextensions.htm
tech.root: gpmc
ms.assetid: 5bcf76f5-f216-4a33-9ac1-4cb98eb26db5
ms.date: 12/05/2018
ms.keywords: GPM object [GPMC],GetClientSideExtensions method, GetClientSideExtensions, GetClientSideExtensions method [GPMC], GetClientSideExtensions method [GPMC],GPM object, GetClientSideExtensions method [GPMC],IGPM interface, IGPM interface [GPMC],GetClientSideExtensions method, IGPM.GetClientSideExtensions, IGPM::GetClientSideExtensions, _win32_igpm_getclientsideextensions, gpmc.igpm_getclientsideextensions, gpmgmt/IGPM::GetClientSideExtensions
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
 - IGPM::GetClientSideExtensions
 - gpmgmt/IGPM::GetClientSideExtensions
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
 - IGPM.GetClientSideExtensions
 - GPM.GetClientSideExtensions
---

# IGPM::GetClientSideExtensions


## -description

Creates and returns a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmcsecollection">GPMCSECollection</a> object that allows you to enumerate Group Policy client-side extensions (CSEs) that are registered on the local computer.

## -parameters

### -param ppIGPMCSECollection [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmcsecollection">IGPMCSECollection</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMCSECollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMCSECollection</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmcsecollection">IGPMCSECollection</a>