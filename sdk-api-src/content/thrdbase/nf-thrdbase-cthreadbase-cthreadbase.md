---
UID: NF:thrdbase.CThreadBase.CThreadBase
title: CThreadBase::CThreadBase
author: windows-sdk-content
description: The CThreadBase::CThreadBase constructor initializes a new instance of CThreadBase. CThreadBase is called internally.
old-location: wmi\cthreadbase_cthreadbase.htm
tech.root: WmiSdk
ms.assetid: 43909501-0a65-4728-9a26-30b8391a33c5
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "??0CThreadBase@@QAE@W4THREAD_SAFETY_MECHANISM@0@@Z, CThreadBase, CThreadBase interface [Windows Management Instrumentation],CThreadBase method, CThreadBase method [Windows Management Instrumentation], CThreadBase method [Windows Management Instrumentation],CThreadBase interface, CThreadBase.CThreadBase, CThreadBase::CThreadBase, thrdbase/CThreadBase::CThreadBase, wmi.cthreadbase_cthreadbase"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: thrdbase.h
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
 - CThreadBase.CThreadBase
 - ??0CThreadBase@@QAE@W4THREAD_SAFETY_MECHANISM@0@@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- thrdbase.h
: 
- CThreadBase.CThreadBase
: 
---

# CThreadBase::CThreadBase


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/0511cd5b-f791-4821-8d75-23b0635e2266">CThreadBase</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>CThreadBase::CThreadBase</b>  constructor initializes a new instance of <a href="https://msdn.microsoft.com/0511cd5b-f791-4821-8d75-23b0635e2266">CThreadBase</a>. <b>CThreadBase</b> is called internally.


## -parameters




### -param etsm

TBD




#### - etsm = etsmSerialized

The thread safety mechanism. The possible values are:

<b>etsmFirst</b>
<b>etsmSerialized</b>
<b>etsmPriorityRead</b>
<b>etsmPriorityWrite</b>
<b>etsmLast</b>

## -returns



This method does not return a value.




## -remarks



The destructor for the class is <b>CThreadBase::~CThreadBase</b>.



