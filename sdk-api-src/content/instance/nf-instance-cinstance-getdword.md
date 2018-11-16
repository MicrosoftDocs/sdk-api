---
UID: NF:instance.CInstance.GetDWORD
title: CInstance::GetDWORD
author: windows-sdk-content
description: The GetDWORD method retrieves a DWORD property.
old-location: wmi\cinstance_getdword.htm
tech.root: WmiSdk
ms.assetid: 02690232-a887-4de3-a850-84ad8ffa9ee0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "?GetDWORD@CInstance@@QBE_NPBGAAK@Z, ?GetDWORD@CInstance@@QEBA_NPEBGAEAK@Z, CInstance interface [Windows Management Instrumentation],GetDWORD method, CInstance.GetDWORD, CInstance::GetDWORD, GetDWORD, GetDWORD method [Windows Management Instrumentation], GetDWORD method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getdword, instance/CInstance::GetDWORD, wmi.cinstance_getdword"
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
 - CInstance.GetDWORD
 - ?GetDWORD@CInstance@@QBE_NPBGAAK@Z
 - ?GetDWORD@CInstance@@QEBA_NPEBGAEAK@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- instance.h
: 
- CInstance.GetDWORD
: 
---

# CInstance::GetDWORD


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetDWORD</b> method retrieves a <b>DWORD</b> property.


## -parameters




### -param name

Name of the <b>DWORD</b> property retrieved.


### -param d [ref]

Buffer to receive the <b>DWORD</b> property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a property that is not a type that is <b>DWORD</b>-compatible or a property that does not exist. More information is available in the log file, Framework.log.



