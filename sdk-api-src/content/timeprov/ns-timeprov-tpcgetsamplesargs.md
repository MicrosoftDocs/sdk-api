---
UID: NS:timeprov.TpcGetSamplesArgs
title: TpcGetSamplesArgs
author: windows-sdk-content
description: A structure that is used by the TimeProvCommand function.
old-location: base\tpcgetsamplesargs_str.htm
tech.root: sysinfo
ms.assetid: 7e92a7c1-6927-4d53-8252-6bdd424d6e0c
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: TpcGetSamplesArgs, TpcGetSamplesArgs structure, _win32_tpcgetsamplesargs_str, base.tpcgetsamplesargs_str, timeprov/TpcGetSamplesArgs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: timeprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Timeprov.h
api_name:
 - TpcGetSamplesArgs
product: Windows
targetos: Windows
req.typenames: TpcGetSamplesArgs
req.redist: 
---

# TpcGetSamplesArgs structure


## -description


A structure that is used by the 
<a href="https://msdn.microsoft.com/07b0bdf2-d224-4bbc-be29-9032a848d5ae">TimeProvCommand</a> function.


## -struct-fields




### -field pbSampleBuf

An array of 
<a href="https://msdn.microsoft.com/020a6502-3357-4800-8fc4-0d73ae42aa51">TimeSample</a> structures.


### -field cbSampleBuf

The size of <b>pbSampleBuf</b>, in bytes.


### -field dwSamplesReturned

The number of samples returned.


### -field dwSamplesAvailable

The total number of samples available.


## -see-also




<a href="https://msdn.microsoft.com/07b0bdf2-d224-4bbc-be29-9032a848d5ae">TimeProvCommand</a>



<a href="https://msdn.microsoft.com/020a6502-3357-4800-8fc4-0d73ae42aa51">TimeSample</a>
 

 

