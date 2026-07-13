---
UID: NF:cfgmgr32.CM_Get_Version_Ex
title: CM_Get_Version_Ex function (cfgmgr32.h)
description: The CM_Get_Version_Ex function returns version 4.0 of the Plug and Play (PnP) Configuration Manager DLL (Cfgmgr32.dll) for a local or a remote machine.
helpviewer_keywords: ["CM_Get_Version_Ex","CM_Get_Version_Ex function [Device and Driver Installation]","cfgmgr32/CM_Get_Version_Ex","cfgmgrfn_0c27aa6b-5682-4901-b57b-2477a0cb9919.xml","devinst.cm_get_version_ex"]
old-location: devinst\cm_get_version_ex.htm
tech.root: devinst
ms.assetid: f189a417-48a4-436e-bb1c-6b0c9f066c04
ms.date: 12/05/2018
ms.keywords: CM_Get_Version_Ex, CM_Get_Version_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Version_Ex, cfgmgrfn_0c27aa6b-5682-4901-b57b-2477a0cb9919.xml, devinst.cm_get_version_ex
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
 - CM_Get_Version_Ex
 - cfgmgr32/CM_Get_Version_Ex
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
 - CM_Get_Version_Ex
---

# CM_Get_Version_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.]

The <b>CM_Get_Version_Ex</b> function returns version 4.0 of the <a href="/windows/win32/api/cfgmgr32/">Plug and Play (PnP) Configuration Manager DLL</a> (<i>Cfgmgr32.dll</i>) for a local or a remote machine.

## -parameters

### -param hMachine [in, optional]

Supplies a machine handle that is returned by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the function succeeds, it returns the major revision number in the high-order byte and the minor revision number in the low-order byte. Version 4.0 is returned as 0x0400. By default, version 4.0 is supported  by Microsoft Windows 2000 and later versions of Windows. If an internal error occurs, the function returns 0x0000. Call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to obtain the error code for the failure.

## -remarks

This function returns version 4.0 of the configuration manager to ensure compatibility with version 4.0 and all later versions of the configuration manager, and to ensure compatibility with all applications that require version 4.0 of the configuration manager.

To determine if a specific version of the configuration manager is available on a machine, use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_version_available">CM_Is_Version_Available</a> or <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex">CM_Is_Version_Available_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_version">CM_Get_Version</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_version_available">CM_Is_Version_Available</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex">CM_Is_Version_Available_Ex</a>