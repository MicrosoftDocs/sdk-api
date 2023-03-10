---
UID: NF:gpmgmt.IGPM.GetRSOP
title: IGPM::GetRSOP (gpmgmt.h)
description: Creates and returns a GPMRSOP. You can specify the Resultant Set of Policy (RSoP) mode and a Windows Management Instrumentation (WMI) namespace.
helpviewer_keywords: ["GPM object [GPMC]","GetRSOP method","GetRSOP","GetRSOP method [GPMC]","GetRSOP method [GPMC]","GPM object","GetRSOP method [GPMC]","IGPM interface","IGPM interface [GPMC]","GetRSOP method","IGPM.GetRSOP","IGPM::GetRSOP","_win32_igpm_getrsop","gpmc.igpm_getrsop","gpmgmt/IGPM::GetRSOP","rsopLogging","rsopPlanning","rsopUnknown"]
old-location: gpmc\igpm_getrsop.htm
tech.root: gpmc
ms.assetid: 61a1be3e-d959-47e2-ad6c-ca00accd0afe
ms.date: 12/05/2018
ms.keywords: GPM object [GPMC],GetRSOP method, GetRSOP, GetRSOP method [GPMC], GetRSOP method [GPMC],GPM object, GetRSOP method [GPMC],IGPM interface, IGPM interface [GPMC],GetRSOP method, IGPM.GetRSOP, IGPM::GetRSOP, _win32_igpm_getrsop, gpmc.igpm_getrsop, gpmgmt/IGPM::GetRSOP, rsopLogging, rsopPlanning, rsopUnknown
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
 - IGPM::GetRSOP
 - gpmgmt/IGPM::GetRSOP
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
 - IGPM.GetRSOP
 - GPM.GetRSOP
---

# IGPM::GetRSOP


## -description

Creates and returns an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">GPMRSOP</a>. You can specify the Resultant Set of Policy (RSoP) mode and a Windows Management Instrumentation (WMI) namespace.

## -parameters

### -param gpmRSoPMode [in]

Required. Mode in which to open the object. The following modes are supported.



#### rsopPlanning

Specifies RSoP planning mode



#### rsopLogging

Specifies RSoP logging mode



#### rsopUnknown

Valid only if the <i>bstrNamespace</i> parameter is specified

To perform the query, RSoP planning mode requires a domain controller that is running Windows Server.

### -param bstrNamespace [in]

WMI namespace for the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">IGPMRSOP</a><b>GPMRSOP</b><b>GPMRSOP</b>.  Use a null-terminated string. This parameter can be <b>NULL</b>. For more information about how to retrieve the namespace, see the "Remarks" section.

### -param lFlags [in]

This parameter must be zero.

### -param ppIGPMRSOP [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">IGPMRSOP</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">GPMRSOP</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">GPMRSOP</a> object.

## -remarks

To retrieve the WMI namespace, call the 
<a href="/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">Namespace</a> property method of the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">IGPMRSOP</a> interface. Or, call the <b>RsopCreateSession</b> method of the 
<a href="/previous-versions/windows/desktop/Policy/rsoploggingmodeprovider">RsopLoggingModeProvider</a> and 
<a href="/previous-versions/windows/desktop/Policy/rsopplanningmodeprovider">RsopPlanningModeProvider</a> WMI classes. For more information about these methods, see the <a href="/previous-versions/windows/desktop/Policy/group-policy-start-page">Group Policy</a> documentation.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">IGPMRSOP</a>