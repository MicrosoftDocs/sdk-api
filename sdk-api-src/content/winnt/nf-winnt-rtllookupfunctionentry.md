---
UID: NF:winnt.RtlLookupFunctionEntry
title: RtlLookupFunctionEntry function
author: windows-sdk-content
description: Searches the active function tables for an entry that corresponds to the specified PC value.
old-location: base\rtllookupfunctionentry.htm
tech.root: debug
ms.assetid: 624b97fb-0453-4f47-b6bd-92aa14705e78
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: RtlLookupFunctionEntry, RtlLookupFunctionEntry function, base.rtllookupfunctionentry, winnt/RtlLookupFunctionEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-rtlsupport-l1-1-0.dll
 - ntdll.dll
 - API-MS-Win-Core-rtlsupport-l1-2-0.dll
api_name:
 - RtlLookupFunctionEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RtlLookupFunctionEntry
: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RtlLookupFunctionEntry function


## -description


Searches the active function tables for an entry that corresponds to the specified PC 
   value.


## -parameters




### -param ControlPc [in]

The virtual address of an instruction bundle within the function.


### -param ImageBase [out]

The base address of module to which the function belongs.


### -param HistoryTable [out]

The global pointer value of the module.

This parameter has a different declaration on x64 and ARM systems. For more information, see x64 Definition 
        and ARM Definition.


## -returns



If there is no entry in the function table for the specified PC, the function returns 
      <b>NULL</b>. Otherwise, the function returns the address of the function table entry that 
      corresponds to the specified PC.




## -see-also




<a href="https://msdn.microsoft.com/3d2d8778-311e-4cc1-b280-4f83ab457755">RtlUnwindEx</a>



<a href="https://msdn.microsoft.com/78d60f7a-0e16-4856-8aca-c251ab066b83">RtlVirtualUnwind</a>
 

 

