---
UID: NF:instance.CInstance.SetWBEMINT64(LPCWSTR,const ULONGLONG)
title: CInstance::SetWBEMINT64(LPCWSTR,const ULONGLONG)
author: windows-sdk-content
description: The SetWBEMINT64(LPCWSTR, const LONGLONG&) method sets a 64-bit integer value.
old-location: wmi\cinstance_setwbemint64_lpcwstr__const_longlong_.htm
tech.root: WmiSdk
ms.assetid: dd06ecb9-0a7f-4487-8143-80418d28f3bb
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetWBEMINT64 method, CInstance.SetWBEMINT64, CInstance.SetWBEMINT64(LPCWSTR,const ULONGLONG), CInstance::SetWBEMINT64, CInstance::SetWBEMINT64(LPCWSTR,const LONGLONG&), CInstance::SetWBEMINT64(LPCWSTR,const ULONGLONG), SetWBEMINT64, SetWBEMINT64 method [Windows Management Instrumentation], SetWBEMINT64 method [Windows Management Instrumentation],CInstance interface, instance/CInstance::SetWBEMINT64, wmi.cinstance_setwbemint64_lpcwstr__const_longlong_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - CInstance.SetWBEMINT64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CInstance::SetWBEMINT64(LPCWSTR,const ULONGLONG)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
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




<a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a>



<a href="https://msdn.microsoft.com/b51d0c51-3b72-4358-8fc3-d1dbc298b4d9">CInstance::GetWBEMINT64</a>
 

 

