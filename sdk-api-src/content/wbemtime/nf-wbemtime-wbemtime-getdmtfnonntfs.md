---
UID: NF:wbemtime.WBEMTime.GetDMTFNonNtfs
title: WBEMTime::GetDMTFNonNtfs method
author: windows-driver-content
description: The GetDMTFNonNtfs method gets a DMTF date in a CIM Date and Time Format from a FAT that does not have time zones.
old-location: wmi\wbemtime_getdmtfnonntfs.htm
old-project: WmiSdk
ms.assetid: 40353352-da1f-44d8-a2c3-e6fd4639bd98
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: "?GetDMTFNonNtfs@WBEMTime@@QBEPAGXZ, ?GetDMTFNonNtfs@WBEMTime@@QEBAPEAGXZ, GetDMTFNonNtfs method [Windows Management Instrumentation], GetDMTFNonNtfs method [Windows Management Instrumentation], WBEMTime interface, GetDMTFNonNtfs,WBEMTime.GetDMTFNonNtfs, WBEMTime, WBEMTime interface [Windows Management Instrumentation], GetDMTFNonNtfs method, WBEMTime::GetDMTFNonNtfs, _hmm_wbemtime_getdmtfnonntfs, wbemtime/WBEMTime::GetDMTFNonNtfs, wmi.wbemtime_getdmtfnonntfs"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WbemTimeout
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	WBEMTime.GetDMTFNonNtfs
-	?GetDMTFNonNtfs@WBEMTime@@QBEPAGXZ
-	?GetDMTFNonNtfs@WBEMTime@@QEBAPEAGXZ
product: Windows
targetos: Windows
req.lib: 
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WBEMTime::GetDMTFNonNtfs method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetDMTFNonNtfs</b> method gets a DMTF date in a 
CIM <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a> from a FAT that does not have time zones.


## -parameters






## -returns



Returns a <b>BSTR</b> in <a href="https://msdn.microsoft.com/be239bf8-88a3-47bc-ae4f-49a5195e7a7d">Date and Time Format</a>.




## -remarks



The calling function must call <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> on the return value.

The time property of <a href="https://msdn.microsoft.com/b633bc8c-9d02-4bcf-8528-10773fb5ae7a">WBEMTime</a> is held in GMT. The <b>GetDMTFNonNtfs</b> method adjusts this time to local time, converts it to a DMTF string, and sets the UTC to "***".  This is compatible with the Microsoft Windows API methods which return time without being time-zone aware.



