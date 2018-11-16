---
UID: NF:chstring.CHString.AllocSysString
title: CHString::AllocSysString
author: windows-sdk-content
description: The AllocSysString method allocates a new BSTR string that is Automation compatible. It then copies the contents of the CHStringstring into it, including the terminating NULL character.
old-location: wmi\chstring_allocsysstring.htm
tech.root: WmiSdk
ms.assetid: 21eb9990-a07f-4d6c-b674-dc35f395e603
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AllocSysString, AllocSysString method [Windows Management Instrumentation], AllocSysString method [Windows Management Instrumentation],CHString interface, CHString interface [Windows Management Instrumentation],AllocSysString method, CHString.AllocSysString, CHString::AllocSysString, _hmm_chstring_allocsysstring, chstring/CHString::AllocSysString, wmi.chstring_allocsysstring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: chstring.h
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
 - CHString.AllocSysString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- chstring.h
: 
- CHString.AllocSysString
: 
---

# CHString::AllocSysString


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>AllocSysString</b> method allocates a new <b>BSTR</b> string that is Automation compatible. It then copies the contents of the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>string into it, including the terminating <b>NULL</b> character.


## -parameters






## -returns



If the <b>AllocSysString</b> method is successful, it points to the newly allocated string.



