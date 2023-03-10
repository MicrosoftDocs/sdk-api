---
UID: NF:gpmgmt.IGPMWMIFilter.GetSecurityInfo
title: IGPMWMIFilter::GetSecurityInfo (gpmgmt.h)
description: Returns an interface or object that represents the list of permissions for the current WMI filter.
helpviewer_keywords: ["GPMWMIFilter class [GPMC]","GetSecurityInfo method","GetSecurityInfo","GetSecurityInfo method [GPMC]","GetSecurityInfo method [GPMC]","GPMWMIFilter class","GetSecurityInfo method [GPMC]","IGPMWMIFilter interface","IGPMWMIFilter interface [GPMC]","GetSecurityInfo method","IGPMWMIFilter.GetSecurityInfo","IGPMWMIFilter::GetSecurityInfo","_win32_igpmwmifilter_getsecurityinfo","gpmc.igpmwmifilter_getsecurityinfo","gpmgmt/IGPMWMIFilter::GetSecurityInfo"]
old-location: gpmc\igpmwmifilter_getsecurityinfo.htm
tech.root: gpmc
ms.assetid: c576c842-53ce-40af-8dba-4f15e25cf493
ms.date: 12/05/2018
ms.keywords: GPMWMIFilter class [GPMC],GetSecurityInfo method, GetSecurityInfo, GetSecurityInfo method [GPMC], GetSecurityInfo method [GPMC],GPMWMIFilter class, GetSecurityInfo method [GPMC],IGPMWMIFilter interface, IGPMWMIFilter interface [GPMC],GetSecurityInfo method, IGPMWMIFilter.GetSecurityInfo, IGPMWMIFilter::GetSecurityInfo, _win32_igpmwmifilter_getsecurityinfo, gpmc.igpmwmifilter_getsecurityinfo, gpmgmt/IGPMWMIFilter::GetSecurityInfo
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
 - IGPMWMIFilter::GetSecurityInfo
 - gpmgmt/IGPMWMIFilter::GetSecurityInfo
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
 - IGPMWMIFilter.GetSecurityInfo
 - GPMWMIFilter.GetSecurityInfo
---

# IGPMWMIFilter::GetSecurityInfo


## -description

Returns an interface or object that represents the list of permissions for the current WMI filter.

## -parameters

### -param ppSecurityInfo [out]

Address of a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">GPMSecurityInfo</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">GPMSecurityInfo</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">IGPMWMIFilterCollection</a>