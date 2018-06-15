---
UID: NF:wbemtime.WBEMTime.GetDMTF
title: WBEMTime::GetDMTF
author: windows-sdk-content
description: The GetDMTF method converts a BSTR value to CIM Date and Time Format.
old-location: wmi\wbemtime_getdmtf.htm
old-project: WmiSdk
ms.assetid: 3bfcf7f8-0b0c-4a3f-83c7-be4c37753a7a
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "?GetDMTF@WBEMTime@@QBEPAGH@Z, ?GetDMTF@WBEMTime@@QEBAPEAGH@Z, GetDMTF, GetDMTF method [Windows Management Instrumentation], GetDMTF method [Windows Management Instrumentation],WBEMTime interface, WBEMTime interface [Windows Management Instrumentation],GetDMTF method, WBEMTime.GetDMTF, WBEMTime::GetDMTF, _hmm_wbemtime_getdmtf, wbemtime/WBEMTime::GetDMTF, wmi.wbemtime_getdmtf"
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
 - WBEMTime.GetDMTF
 - ?GetDMTF@WBEMTime@@QBEPAGH@Z
 - ?GetDMTF@WBEMTime@@QEBAPEAGH@Z
product: Windows
targetos: Windows
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WBEMTime::GetDMTF


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetDMTF</b> method converts a  <b>BSTR</b> value to 
CIM <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.


## -parameters




### -param bLocal

If <b>TRUE</b>, returns the local time, adjusted for daylight savings time; otherwise, returns GMT.


## -returns



Returns a <b>BSTR</b> in <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.




## -remarks



The calling function must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> on the return value.




## -see-also




<a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a>



<a href="https://msdn.microsoft.com/f1fe92cc-1d51-4bd7-950b-84c76b001163">WBEMTime::GetBSTR</a>



<a href="https://msdn.microsoft.com/5a2ed11d-34d8-44b1-a8ce-e8aa7c96c730">WBEMTime::SetDMTF</a>
 

 

