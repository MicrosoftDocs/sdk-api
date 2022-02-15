---
UID: NF:chstring.CHString.AllocSysString
title: CHString::AllocSysString (chstring.h)
description: The AllocSysString method allocates a new BSTR string that is Automation compatible. It then copies the contents of the CHStringstring into it, including the terminating NULL character.
helpviewer_keywords: ["AllocSysString","AllocSysString method [Windows Management Instrumentation]","AllocSysString method [Windows Management Instrumentation]","CHString interface","CHString interface [Windows Management Instrumentation]","AllocSysString method","CHString.AllocSysString","CHString::AllocSysString","_hmm_chstring_allocsysstring","chstring/CHString::AllocSysString","wmi.chstring_allocsysstring"]
old-location: wmi\chstring_allocsysstring.htm
tech.root: wmi
ms.assetid: 21eb9990-a07f-4d6c-b674-dc35f395e603
ms.date: 12/05/2018
ms.keywords: AllocSysString, AllocSysString method [Windows Management Instrumentation], AllocSysString method [Windows Management Instrumentation],CHString interface, CHString interface [Windows Management Instrumentation],AllocSysString method, CHString.AllocSysString, CHString::AllocSysString, _hmm_chstring_allocsysstring, chstring/CHString::AllocSysString, wmi.chstring_allocsysstring
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CHString::AllocSysString
 - chstring/CHString::AllocSysString
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
 - CHString.AllocSysString
---

# CHString::AllocSysString


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/WmiSdk/chstring">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>AllocSysString</b> method allocates a new <b>BSTR</b> string that is Automation compatible. It then copies the contents of the <a href="/windows/desktop/WmiSdk/chstring">CHString</a> string into it, including the terminating <b>NULL</b> character.



## -returns

If the <b>AllocSysString</b> method is successful, it points to the newly allocated string.
