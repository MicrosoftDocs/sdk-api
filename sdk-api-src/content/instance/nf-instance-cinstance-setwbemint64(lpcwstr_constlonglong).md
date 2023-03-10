---
UID: NF:instance.CInstance.SetWBEMINT64(LPCWSTR,constLONGLONG)
title: CInstance::SetWBEMINT64(LPCWSTR,const LONGLONG) (instance.h)
description: The SetWBEMINT64(LPCWSTR, const LONGLONG&) method sets a 64-bit integer value. (overload 3/3)
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","SetWBEMINT64 method","CInstance.SetWBEMINT64","CInstance.SetWBEMINT64(LPCWSTR","const LONGLONG)","CInstance::SetWBEMINT64","CInstance::SetWBEMINT64(LPCWSTR","const LONGLONG&)","CInstance::SetWBEMINT64(LPCWSTR","const LONGLONG)","SetWBEMINT64","SetWBEMINT64 method [Windows Management Instrumentation]","SetWBEMINT64 method [Windows Management Instrumentation]","CInstance interface","instance/CInstance::SetWBEMINT64","wmi.cinstance_setwbemint64_lpcwstr__const_longlong_"]
old-location: wmi\cinstance_setwbemint64_lpcwstr__const_longlong_.htm
tech.root: wmi
ms.assetid: dd06ecb9-0a7f-4487-8143-80418d28f3bb
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetWBEMINT64 method, CInstance.SetWBEMINT64, CInstance.SetWBEMINT64(LPCWSTR,const LONGLONG), CInstance::SetWBEMINT64, CInstance::SetWBEMINT64(LPCWSTR,const LONGLONG&), CInstance::SetWBEMINT64(LPCWSTR,const LONGLONG), SetWBEMINT64, SetWBEMINT64 method [Windows Management Instrumentation], SetWBEMINT64 method [Windows Management Instrumentation],CInstance interface, instance/CInstance::SetWBEMINT64, wmi.cinstance_setwbemint64_lpcwstr__const_longlong_
req.header: instance.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CInstance::SetWBEMINT64
 - instance/CInstance::SetWBEMINT64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.SetWBEMINT64
---

## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetWBEMINT64(LPCWSTR, const LONGLONG&amp;)</b> method sets a 64-bit integer value.

## -parameters

### -param name

Name of the 64-bit integer property that is set.

### -param i64Value [ref]

Value assigned to the 64-bit integer property.

## -returns

Returns <b>TRUE</b> if the operation is successful and <b>FALSE</b> if an attempt was made to set a nonexistent property or a property that is not a 64-bit integer.  More information is available in the log file, Framework.log.

## -remarks

The provider framework currently uses a CHString type to set the 64-bit integer  rather than a WBEMINT64 type.

## -see-also

<a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a>



<a href="/windows/desktop/WmiSdk/cinstance-getwbemint64">CInstance::GetWBEMINT64</a>
