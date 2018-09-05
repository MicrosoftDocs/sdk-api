---
UID: NF:instance.CInstance.SetWCHARSplat
title: CInstance::SetWCHARSplat
author: windows-sdk-content
description: The SetWCHARSplat method sets a string property.
old-location: wmi\cinstance_setwcharsplat.htm
old-project: WmiSdk
ms.assetid: 3c565630-3626-4d60-9bd2-74c2218bec11
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetWCHARSplat method, CInstance.SetWCHARSplat, CInstance::SetWCHARSplat, SetWCHARSplat, SetWCHARSplat method [Windows Management Instrumentation], SetWCHARSplat method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setwcharsplat, instance/CInstance::SetWCHARSplat, wmi.cinstance_setwcharsplat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: instance.h
req.include-header: FwCommon.h
req.redist: 
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
req.typenames: TrustLevel
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.SetWCHARSplat
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: GDI+ 1.1
---

# CInstance::SetWCHARSplat


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetWCHARSplat</b> method sets a string property.


## -parameters




### -param name

Name of the string property to be modified.


### -param pStr

Pointer to the Unicode string.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-string property. More information is available in the log file, Framework.log.



