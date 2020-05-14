---
UID: NS:opmapi._OPM_RANDOM_NUMBER
title: OPM_RANDOM_NUMBER (opmapi.h)
description: Contains a 128-bit random number for use with Output Protection Manager (OPM).helpviewer_keywords: ["OPM_RANDOM_NUMBER","OPM_RANDOM_NUMBER structure [Media Foundation]","_OPM_RANDOM_NUMBER","ksopmapi/OPM_RANDOM_NUMBER","mf.opm_random_number"]
old-location: mf\opm_random_number.htm
tech.root: medfound
ms.assetid: d3a5be4b-39d1-43da-b87e-ab4dd7815262
ms.date: 12/05/2018
ms.keywords: OPM_RANDOM_NUMBER, OPM_RANDOM_NUMBER structure [Media Foundation], _OPM_RANDOM_NUMBER, ksopmapi/OPM_RANDOM_NUMBER, mf.opm_random_number
f1_keywords:
- opmapi/OPM_RANDOM_NUMBER
dev_langs:
- c++
req.header: opmapi.h
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
targetos: Windows
req.typenames: OPM_RANDOM_NUMBER
req.redist: 
ms.custom: 19H1
---

# OPM_RANDOM_NUMBER structure


## -description


Contains a 128-bit random number for use with <a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM).


## -struct-fields




### -field abRandomNumber

A 128-bit array that contains a random number. 


## -remarks



Always use a cryptographically secure random-number generator to fill in this structure. The <b>CryptGenRandom</b> function is recommended, although not required.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
 

 

