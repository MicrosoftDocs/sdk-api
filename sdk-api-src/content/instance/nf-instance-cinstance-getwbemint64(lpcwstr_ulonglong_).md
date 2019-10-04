---
UID: NF:instance.CInstance.GetWBEMINT64(LPCWSTR,ULONGLONG &)
title: CInstance::GetWBEMINT64(LPCWSTR,ULONGLONG &) (instance.h)
author: windows-sdk-content
description: The GetWBEMINT64 method retrieves a 64-bit integer property.
old-location: wmi\cinstance_getwbemint64_lpcwstr__longlong__.htm
tech.root: WmiSdk
ms.assetid: b585e740-eade-4f81-908c-98dd88540cb1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],GetWBEMINT64 method, CInstance.GetWBEMINT64, CInstance.GetWBEMINT64(LPCWSTR,ULONGLONG &), CInstance::GetWBEMINT64, CInstance::GetWBEMINT64(LPCWSTR,LONGLONG&), CInstance::GetWBEMINT64(LPCWSTR,ULONGLONG &), GetWBEMINT64, GetWBEMINT64 method [Windows Management Instrumentation], GetWBEMINT64 method [Windows Management Instrumentation],CInstance interface, instance/CInstance::GetWBEMINT64, wmi.cinstance_getwbemint64_lpcwstr__longlong__
ms.topic: method
f1_keywords: 
 - "instance/CInstance.GetWBEMINT64"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.GetWBEMINT64
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CInstance::GetWBEMINT64(LPCWSTR,ULONGLONG &)


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetWBEMINT64</b> method retrieves a 64-bit integer property.


## -parameters




### -param name

Name of the 64-bit integer property retrieved.


### -param i64Value

TBD




#### - wbemint64 [ref]

Buffer to receive the 64-bit integer value.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent  property or a property that is not a 64-bit integer.  More information is available in the log file, Framework.log.




## -remarks



The provider framework currently returns a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring">CHString</a> value rather than a <b>WBEMINT64</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/cinstance-getwbemint64">CInstance::GetWBEMINT64</a>
 

 

