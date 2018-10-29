---
UID: NS:ksopmapi._OPM_RANDOM_NUMBER
title: "_OPM_RANDOM_NUMBER"
author: windows-sdk-content
description: Contains a 128-bit random number for use with Output Protection Manager (OPM).
old-location: mf\opm_random_number.htm
tech.root: medfound
ms.assetid: d3a5be4b-39d1-43da-b87e-ab4dd7815262
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*POPM_RANDOM_NUMBER, OPM_RANDOM_NUMBER, OPM_RANDOM_NUMBER structure [Media Foundation], _OPM_RANDOM_NUMBER, ksopmapi/OPM_RANDOM_NUMBER, mf.opm_random_number"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ksopmapi.h
req.include-header: Opmapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ksopmapi.h
api_name:
 - OPM_RANDOM_NUMBER
product: Windows
targetos: Windows
req.typenames: OPM_RANDOM_NUMBER, *POPM_RANDOM_NUMBER
req.redist: 
---

# _OPM_RANDOM_NUMBER structure


## -description


Contains a 128-bit random number for use with <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a> (OPM).


## -struct-fields




### -field abRandomNumber

A 128-bit array that contains a random number. 


## -remarks



Always use a cryptographically secure random-number generator to fill in this structure. The <b>CryptGenRandom</b> function is recommended, although not required.




## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 

