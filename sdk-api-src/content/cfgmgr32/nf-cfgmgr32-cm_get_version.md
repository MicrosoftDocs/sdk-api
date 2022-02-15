---
UID: NF:cfgmgr32.CM_Get_Version
title: CM_Get_Version function (cfgmgr32.h)
description: The CM_Get_Version function returns version 4.0 of the Plug and Play (PnP) Configuration Manager DLL (Cfgmgr32.dll) for a local machine.
helpviewer_keywords: ["CM_Get_Version","CM_Get_Version function [Device and Driver Installation]","cfgmgr32/CM_Get_Version","cfgmgrfn_505306b1-3e78-4de2-aa51-128fe87c17ed.xml","devinst.cm_get_version"]
old-location: devinst\cm_get_version.htm
tech.root: devinst
ms.assetid: 998c6c57-b242-4aa0-8c9f-cfff61d2a642
ms.date: 12/05/2018
ms.keywords: CM_Get_Version, CM_Get_Version function [Device and Driver Installation], cfgmgr32/CM_Get_Version, cfgmgrfn_505306b1-3e78-4de2-aa51-128fe87c17ed.xml, devinst.cm_get_version
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Get_Version
 - cfgmgr32/CM_Get_Version
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Get_Version
---

# CM_Get_Version function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.]

The <b>CM_Get_Version</b> function returns version 4.0 of the <a href="/windows/win32/api/cfgmgr32/">Plug and Play (PnP) Configuration Manager DLL</a> (<i>Cfgmgr32.dll</i>) for a local machine.



## -returns

If the function succeeds, it returns the major revision number in the high-order byte, and the minor revision number in the low-order byte. Version 4.0 is returned as 0x0400. By default, version 4.0 is supported by Microsoft Windows 2000 and later versions of Windows. If an internal error occurs, the function returns 0x0000. Call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to obtain the error code for the failure.

## -remarks

This function returns version 4.0 of the configuration manager to ensure compatibility with version 4.0 and all later versions of the configuration manager, and to ensure compatibility with all applications that require version 4.0 of the configuration manager.

To determine if a specific version of the configuration manager is available on a machine, use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_version_available">CM_Is_Version_Available</a> or <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex">CM_Is_Version_Available_Ex</a>.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_version_ex">CM_Get_Version_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_version_available">CM_Is_Version_Available</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex">CM_Is_Version_Available_Ex</a>
