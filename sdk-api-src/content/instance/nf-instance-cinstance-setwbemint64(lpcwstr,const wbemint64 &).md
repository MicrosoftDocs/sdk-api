---
UID: NF:instance.CInstance.SetWBEMINT64(LPCWSTR,const WBEMINT64 &)
title: CInstance::SetWBEMINT64(LPCWSTR,const WBEMINT64 &)
author: windows-sdk-content
description: The SetWBEMINT64(LPCWSTR, const WBEMINT64&) method sets a 64-bit integer property.
old-location: wmi\cinstance_setwbemint64_lpcwstr__const_wbemint64__.htm
tech.root: WmiSdk
ms.assetid: 0015f024-19bd-4069-b946-706e9492fbe8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetWBEMINT64 method, CInstance.SetWBEMINT64, CInstance.SetWBEMINT64(LPCWSTR,const WBEMINT64 &), CInstance::SetWBEMINT64, CInstance::SetWBEMINT64(LPCWSTR,const WBEMINT64 &), CInstance::SetWBEMINT64(LPCWSTR,const WBEMINT64&), SetWBEMINT64, SetWBEMINT64 method [Windows Management Instrumentation], SetWBEMINT64 method [Windows Management Instrumentation],CInstance interface, instance/CInstance::SetWBEMINT64, wmi.cinstance_setwbemint64_lpcwstr__const_wbemint64__
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

# CInstance::SetWBEMINT64(LPCWSTR,const WBEMINT64 &)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetWBEMINT64(LPCWSTR, const WBEMINT64&amp;)</b> method sets a 64-bit integer property.


## -parameters




### -param name

Name of the 64-bit integer property that is set.


### -param wbemint64

TBD




#### - i64Value [ref]

Value assigned to the 64-bit integer property.


## -returns



Returns <b>TRUE</b> if the operation is successful and <b>FALSE</b> if an attempt was made to set a nonexistent property or a property that is not a 64-bit integer.  More information is available in the log file, Framework.log.




## -remarks



The provider framework currently uses a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> type to set the 64-bit integer rather than a <b>WBEMINT64</b> type.




## -see-also




<a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a>



<a href="https://msdn.microsoft.com/b51d0c51-3b72-4358-8fc3-d1dbc298b4d9">CInstance::GetWBEMINT64</a>
 

 

