---
UID: NF:wbemtime.WBEMTime.GetBSTR
title: WBEMTime::GetBSTR
author: windows-sdk-content
description: Gets the time as a BSTR value in CIM Date and Time Format.
old-location: wmi\wbemtime_getbstr.htm
old-project: WmiSdk
ms.assetid: f1fe92cc-1d51-4bd7-950b-84c76b001163
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "?GetBSTR@WBEMTime@@QBEPAGXZ, ?GetBSTR@WBEMTime@@QEBAPEAGXZ, GetBSTR, GetBSTR method [Windows Management Instrumentation], GetBSTR method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetBSTR method, WBEMTime.GetBSTR, WBEMTime::GetBSTR, _hmm_wbemtime_getbstr, wbemtime/WBEMTime::GetBSTR, wmi.wbemtime_getbstr"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemtime.h
req.include-header: 
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
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - WBEMTime.GetBSTR
 - ?GetBSTR@WBEMTime@@QBEPAGXZ
 - ?GetBSTR@WBEMTime@@QEBAPEAGXZ
product: Windows
targetos: Windows
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WBEMTime::GetBSTR


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetBSTR</b> method gets the time as a <b>BSTR</b> value in 
CIM <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.


## -parameters






## -returns



The method returns a <b>BSTR</b> in <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>. The time is given as GMT. If the internal time value is INVALID_TIME, the method returns <b>NULL</b>.




## -remarks



If the value returned is not <b>NULL</b>, the calling function must call <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> on the returned value. This method returns the same value as <a href="https://msdn.microsoft.com/3bfcf7f8-0b0c-4a3f-83c7-be4c37753a7a">WBEMTime::GetDMTF</a>(false).




## -see-also




<a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a>



<a href="https://msdn.microsoft.com/3bfcf7f8-0b0c-4a3f-83c7-be4c37753a7a">WBEMTime::GetDMTF</a>
 

 

