---
UID: NF:cfgmgr32.CM_Is_Version_Available_Ex
title: CM_Is_Version_Available_Ex function (cfgmgr32.h)
description: The CM_Is_Version_Available_Ex function indicates whether a specified version of the Plug and Play (PNP) Configuration Manager DLL (Cfgmgr32.dll) is supported by a local or a remote machine.
helpviewer_keywords: ["CM_Is_Version_Available_Ex","CM_Is_Version_Available_Ex function [Device and Driver Installation]","cfgmgr32/CM_Is_Version_Available_Ex","cfgmgrfn_12196a98-8bca-4afa-8313-5a51f8c3cae1.xml","devinst.cm_is_version_available_ex"]
old-location: devinst\cm_is_version_available_ex.htm
tech.root: devinst
ms.assetid: a6728f01-7899-46e3-8cda-19a5c46f4992
ms.date: 12/05/2018
ms.keywords: CM_Is_Version_Available_Ex, CM_Is_Version_Available_Ex function [Device and Driver Installation], cfgmgr32/CM_Is_Version_Available_Ex, cfgmgrfn_12196a98-8bca-4afa-8313-5a51f8c3cae1.xml, devinst.cm_is_version_available_ex
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later versions of Windows.
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
 - CM_Is_Version_Available_Ex
 - cfgmgr32/CM_Is_Version_Available_Ex
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
 - CM_Is_Version_Available_Ex
---

# CM_Is_Version_Available_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.]

The <b>CM_Is_Version_Available_Ex</b> function indicates whether a specified version of the <a href="/windows/win32/api/cfgmgr32/">Plug and Play (PnP) Configuration Manager DLL</a> (<i>Cfgmgr32.dll</i>) is supported by a local or a remote machine.

## -parameters

### -param wVersion [in]

Identifies a version of the configuration manager. The supported version of the configuration manager corresponds directly to the operating system version. The major version is specified by the high-order byte and the minor version is specified by the low-order byte. For example, 0x0400 specifies version 4.0, which is supported by default by Microsoft Windows NT 4.0 and later versions of Windows. Version 0x0501 specifies version 5.1, which is supported by Windows XP and later versions of Windows.

### -param hMachine [in, optional]

Supplies a machine handle that is returned by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

The function returns <b>TRUE</b> if the function can connect to the specified machine and if the machine supports the specified version. Otherwise, the function returns <b>FALSE</b>.

## -remarks

Use this function to determine whether a specified version of the configuration manager is supported by a local or a remote machine. If the specified version is supported, all versions earlier and including this version are supported by the machine. You can also use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_version_available">CM_Is_Version_Available</a> to determine if the local machine supports a specific version of the configuration manager. 

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_version">CM_Get_Version</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_version_ex">CM_Get_Version_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_version_available">CM_Is_Version_Available</a>