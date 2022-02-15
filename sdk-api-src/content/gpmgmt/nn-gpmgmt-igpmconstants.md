---
UID: NN:gpmgmt.IGPMConstants
title: IGPMConstants (gpmgmt.h)
description: The IGPMConstants interface supports methods that retrieve the value of multiple Group Policy Management Console (GPMC) constants. To create a GPMConstants object, call the IGPM::GetConstants method.
helpviewer_keywords: ["GPMConstants","IGPMConstants","IGPMConstants interface [GPMC]","IGPMConstants interface [GPMC]","described","_win32_igpmconstants","gpmc.igpmconstants","gpmgmt/IGPMConstants"]
old-location: gpmc\igpmconstants.htm
tech.root: gpmc
ms.assetid: e9137167-4a2d-4cc4-940e-20f9991c4187
ms.date: 12/05/2018
ms.keywords: GPMConstants, IGPMConstants, IGPMConstants interface [GPMC], IGPMConstants interface [GPMC],described, _win32_igpmconstants, gpmc.igpmconstants, gpmgmt/IGPMConstants
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
 - IGPMConstants
 - gpmgmt/IGPMConstants
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
 - IGPMConstants
 - GPMConstants
---

# IGPMConstants interface


## -description

The 
<b>IGPMConstants</b> interface supports methods that retrieve the value of multiple Group Policy Management Console (GPMC) constants. To create a <b>GPMConstants</b> object, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getconstants">IGPM::GetConstants</a> method.

The <b>GPMConstants</b> object that implements the 
<b>IGPMConstants</b> interface does not introduce new constants. All the constant values and enumeration types that are returned by the <b>GPMConstants</b> object can be found in either the GPMC header file (Gpmgmt.idl or Gpmgmt.h) or in the GPMC type library that is embedded in the Gpmgmt.dll dynamic-link library. Use the <b>GPMConstants</b> object only if you do not have access to the header or to the type library.

## -inheritance

The <b>IGPMConstants</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGPMConstants</b> also has these types of members:

## -remarks

Properties that begin with <b>PermGPO</b> apply only to GPOs. Properties that begin with <b>PermWMIFilter</b> apply only to Windows Management Instrumentation (WMI) filters.

For more information about policy-related permissions, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a> (<b>GPM.CreatePermission</b>).

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>
