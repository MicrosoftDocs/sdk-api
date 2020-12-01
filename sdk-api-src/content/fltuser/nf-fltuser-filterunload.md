---
UID: NF:fltuser.FilterUnload
title: FilterUnload function (fltuser.h)
description: An application that has loaded a supporting minifilter by calling FilterLoad can unload the minifilter by calling the FilterUnload function.
helpviewer_keywords: ["FilterUnload","FilterUnload function [Installable File System Drivers]","FltWin32ApiRef_d6c75950-e58b-4f4c-8707-85566c03d219.xml","fltuser/FilterUnload","ifsk.filterunload"]
old-location: ifsk\filterunload.htm
tech.root: ifsk
ms.assetid: 74de2531-1666-420e-b500-131622f1b76f
ms.date: 12/05/2018
ms.keywords: FilterUnload, FilterUnload function [Installable File System Drivers], FltWin32ApiRef_d6c75950-e58b-4f4c-8707-85566c03d219.xml, fltuser/FilterUnload, ifsk.filterunload
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
req.target-min-winverclnt: 
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
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FilterUnload
 - fltuser/FilterUnload
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterUnload
---

# FilterUnload function


## -description

An application that has loaded a supporting minifilter by calling <a href="/windows/desktop/api/fltuser/nf-fltuser-filterload">FilterLoad</a> can unload the minifilter by calling the <b>FilterUnload</b> function.

## -parameters

### -param lpFilterName [in]

Pointer to a null-terminated wide-character string containing the same minifilter name that was passed to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterload">FilterLoad</a>. This parameter is required and cannot be <b>NULL</b> or an empty string.

## -returns

<b>FilterUnload</b> returns S_OK if successful. Otherwise, it returns an error value.

## -remarks

<b>FilterUnload</b> is the Win32 equivalent of <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltunloadfilter">FltUnloadFilter</a>. 

<b>FilterUnload</b> searches for a registered minifilter whose service name matches the given <i>lpFilterName</i> and calls that minifilter's <i>FilterUnloadCallback</i> (<a href="/windows-hardware/drivers/ddi/content/fltkernel/nc-fltkernel-pflt_filter_unload_callback">PFLT_FILTER_UNLOAD_CALLBACK</a>) routine. 

If the minifilter did not register a <i>FilterUnloadCallback</i> routine, the call to <b>FilterUnload</b> fails. 

Callers of <b>FilterUnload</b> must have <b>SeLoadDriverPrivilege</b> (the LUID of SE_LOAD_DRIVER_PRIVILEGE) to load or unload a minifilter driver. This privilege is named by the SE_LOAD_DRIVER_NAME name constant. (Privileges are described in the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 documentation.)

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterload">FilterLoad</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltunloadfilter">FltUnloadFilter</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nc-fltkernel-pflt_filter_unload_callback">PFLT_FILTER_UNLOAD_CALLBACK</a>