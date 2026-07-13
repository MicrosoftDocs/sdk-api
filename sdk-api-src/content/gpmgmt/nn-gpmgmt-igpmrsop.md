---
UID: NN:gpmgmt.IGPMRSOP
title: IGPMRSOP (gpmgmt.h)
description: The IGPMRSOP interface provides methods that support making Resultant Set of Policy (RSoP) queries in both logging and planning mode.
helpviewer_keywords: ["GPMRSOP","IGPMRSOP","IGPMRSOP interface [GPMC]","IGPMRSOP interface [GPMC]","described","_win32_igpmrsop","gpmc.igpmrsop","gpmgmt/IGPMRSOP"]
old-location: gpmc\igpmrsop.htm
tech.root: gpmc
ms.assetid: 86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3
ms.date: 12/05/2018
ms.keywords: GPMRSOP, IGPMRSOP, IGPMRSOP interface [GPMC], IGPMRSOP interface [GPMC],described, _win32_igpmrsop, gpmc.igpmrsop, gpmgmt/IGPMRSOP
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
 - IGPMRSOP
 - gpmgmt/IGPMRSOP
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
 - IGPMRSOP
 - GPMRSOP
---

# IGPMRSOP interface


## -description

The 
<b>IGPMRSOP</b> interface provides methods that support making Resultant Set of Policy (RSoP) queries in both logging and planning mode. The typical use of this interface is to set various properties required for a particular RSoP query and then to call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-createqueryresults">CreateQueryResults</a> method. RSoP planning mode requires Windows Server on the domain controller used to perform the query. RSoP logging mode requires that the computer being targeted be running Windows Server.
To create a  <b>GPMRSOP</b> object, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getrsop">IGPM::GetRSOP</a> method.

## -inheritance

The <b>IGPMRSOP</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGPMRSOP</b> also has these types of members:

## -remarks

For more information about security groups, see 
<a href="/windows/desktop/AD/how-security-groups-are-used-in-access-control">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>
