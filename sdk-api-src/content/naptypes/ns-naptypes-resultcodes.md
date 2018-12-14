---
UID: NS:naptypes.tagResultCodes
title: ResultCodes
author: windows-sdk-content
description: Defines a list of result codes.
old-location: nap\resultcodes_struct.htm
tech.root: NAP
ms.assetid: 9d608f0a-9841-48e6-8856-2d8c1afc3e5d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ResultCodes, ResultCodes structure [NAP], nap.resultcodes_struct, naptypes/ResultCodes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
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
 - NapTypes.h
api_name:
 - ResultCodes
product: Windows
targetos: Windows
req.typenames: ResultCodes
req.redist: 
---

# ResultCodes structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>ResultCodes</b> structure defines a list of result codes.


## -struct-fields




### -field count

The number of result codes as a number between 0 and <a href="https://msdn.microsoft.com/2727487c-8c6a-4cd9-b6d8-253191a7d7f6">maxDwordCountPerSoHAttribute</a>.


### -field results

A pointer to either a list of application defined 4-octet HRESULTs that specify whether the client machine is compliant, or a list of <a href="https://msdn.microsoft.com/b2fba990-75d9-4153-8058-c01e97700d00">NAP error constants</a> that specify the cause of <a href="https://msdn.microsoft.com/6db0303d-ab33-4fb9-90a2-b909b2781ba5">SoH</a> construction or processing errors. The values must be in the byte ordering of the host system.


## -see-also




<a href="https://msdn.microsoft.com/e391be3c-95ab-4c80-a5d8-8a8fef28e56b">NAP Reference</a>



<a href="https://msdn.microsoft.com/68048587-0f7e-48d4-9326-768a977ea3ee">NAP Structures</a>
 

 

