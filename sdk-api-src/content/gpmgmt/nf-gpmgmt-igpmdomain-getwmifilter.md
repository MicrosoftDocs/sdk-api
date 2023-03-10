---
UID: NF:gpmgmt.IGPMDomain.GetWMIFilter
title: IGPMDomain::GetWMIFilter (gpmgmt.h)
description: Retrieves a GPMWMIFilter object for the specified path.
helpviewer_keywords: ["GPMDomain object [GPMC]","GetWMIFilter method","GetWMIFilter","GetWMIFilter method [GPMC]","GetWMIFilter method [GPMC]","GPMDomain object","GetWMIFilter method [GPMC]","IGPMDomain interface","IGPMDomain interface [GPMC]","GetWMIFilter method","IGPMDomain.GetWMIFilter","IGPMDomain::GetWMIFilter","_win32_igpmdomain_getwmifilter","gpmc.igpmdomain_getwmifilter","gpmgmt/IGPMDomain::GetWMIFilter"]
old-location: gpmc\igpmdomain_getwmifilter.htm
tech.root: gpmc
ms.assetid: 093fba1a-69b3-4045-891a-de9c6a78e166
ms.date: 12/05/2018
ms.keywords: GPMDomain object [GPMC],GetWMIFilter method, GetWMIFilter, GetWMIFilter method [GPMC], GetWMIFilter method [GPMC],GPMDomain object, GetWMIFilter method [GPMC],IGPMDomain interface, IGPMDomain interface [GPMC],GetWMIFilter method, IGPMDomain.GetWMIFilter, IGPMDomain::GetWMIFilter, _win32_igpmdomain_getwmifilter, gpmc.igpmdomain_getwmifilter, gpmgmt/IGPMDomain::GetWMIFilter
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
 - IGPMDomain::GetWMIFilter
 - gpmgmt/IGPMDomain::GetWMIFilter
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
 - IGPMDomain.GetWMIFilter
 - GPMDomain.GetWMIFilter
---

# IGPMDomain::GetWMIFilter


## -description

Retrieves a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object for the specified path.

## -parameters

### -param bstrPath [in]

Path of the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object to retrieve, in the following format: MSFT_SomFilter.Domain="<i>&lt;domain of the WMI filter&gt;</i>", ID="<i>&lt;GUID that represents the WMI filter&gt;</i>". Consider this example: MSFT_SomFilter.Domain="example.microsoft.com", ID="{7ab06d20-5e0a-4de9-8170-13dea779a528}".

### -param ppWMIFilter [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>