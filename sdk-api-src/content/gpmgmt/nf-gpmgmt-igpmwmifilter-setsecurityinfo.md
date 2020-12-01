---
UID: NF:gpmgmt.IGPMWMIFilter.SetSecurityInfo
title: IGPMWMIFilter::SetSecurityInfo (gpmgmt.h)
description: Sets the list of permissions for the current WMI filter to that specified by the object.
helpviewer_keywords: ["GPMWMIFilter object [GPMC]","SetSecurityInfo method","IGPMWMIFilter interface [GPMC]","SetSecurityInfo method","IGPMWMIFilter.SetSecurityInfo","IGPMWMIFilter::SetSecurityInfo","SetSecurityInfo","SetSecurityInfo method [GPMC]","SetSecurityInfo method [GPMC]","GPMWMIFilter object","SetSecurityInfo method [GPMC]","IGPMWMIFilter interface","_win32_igpmwmifilter_setsecurityinfo","gpmc.igpmwmifilter_setsecurityinfo","gpmgmt/IGPMWMIFilter::SetSecurityInfo"]
old-location: gpmc\igpmwmifilter_setsecurityinfo.htm
tech.root: gpmc
ms.assetid: e03af7ce-dec8-4390-9880-6f5ff050ca0c
ms.date: 12/05/2018
ms.keywords: GPMWMIFilter object [GPMC],SetSecurityInfo method, IGPMWMIFilter interface [GPMC],SetSecurityInfo method, IGPMWMIFilter.SetSecurityInfo, IGPMWMIFilter::SetSecurityInfo, SetSecurityInfo, SetSecurityInfo method [GPMC], SetSecurityInfo method [GPMC],GPMWMIFilter object, SetSecurityInfo method [GPMC],IGPMWMIFilter interface, _win32_igpmwmifilter_setsecurityinfo, gpmc.igpmwmifilter_setsecurityinfo, gpmgmt/IGPMWMIFilter::SetSecurityInfo
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
 - IGPMWMIFilter::SetSecurityInfo
 - gpmgmt/IGPMWMIFilter::SetSecurityInfo
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
 - IGPMWMIFilter.SetSecurityInfo
 - GPMWMIFilter.SetSecurityInfo
---

## -description

Sets the list of permissions for the current WMI filter to that specified by the object.

## -parameters

### -param pSecurityInfo [in]

Pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a> interface.  This parameter is required.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -remarks

You should understand these considerations before changing permissions on WMI filters.

<ul>
<li>Read permission is required for all users to whom a WMI filter applies. Authenticated users always have read access to all WMI filters. Typically, all users to whom the GPO with the WMI filter link applies also have read access.</li>
<li>Users with permission to edit WMI filters can affect policy processing for all users to whom the WMI filter applies.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">IGPMWMIFilterCollection</a>