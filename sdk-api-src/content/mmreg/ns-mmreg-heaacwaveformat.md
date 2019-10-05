---
UID: NS:mmreg.heaacwaveformat_tag
title: HEAACWAVEFORMAT (mmreg.h)
author: windows-sdk-content
description: Contains format data for an AAC or HE-AAC stream that includes AudioSpecificConfig() data.
old-location: dshow\heaacwaveformat.htm
tech.root: DirectShow
ms.assetid: 0809eaa7-3c4c-467d-afa0-d9555ab6d71f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPHEAACWAVEFORMAT, *NPHEAACWAVEFORMAT, *PHEAACWAVEFORMAT, HEAACWAVEFORMAT, HEAACWAVEFORMAT structure [DirectShow], PHEAACWAVEFORMAT, PHEAACWAVEFORMAT structure pointer [DirectShow], dshow.heaacwaveformat, heaacwaveformat_tag, mmreg/HEAACWAVEFORMAT, mmreg/PHEAACWAVEFORMAT"
ms.topic: struct
f1_keywords: 
 - "mmreg/HEAACWAVEFORMAT"
dev_langs:
 - c++
req.header: mmreg.h
req.include-header: 
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
 - mmreg.h
api_name:
 - HEAACWAVEFORMAT
targetos: Windows
req.typenames: HEAACWAVEFORMAT
req.redist: 
ms.custom: 19H1
---

# HEAACWAVEFORMAT structure


## -description


Contains format data for an AAC or HE-AAC stream that includes AudioSpecificConfig() data.


## -struct-fields




### -field wfInfo

A <a href="https://docs.microsoft.com/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo">HEAACWAVEINFO</a> structure. 


### -field pbAudioSpecificConfig

A byte array that contains the value of AudioSpecificConfig(), as defined by ISO/IEC 14496-3. The array might be larger than the size given in the structure declaration. Use the value of <b>wfInfo.wfx.cbSize</b>  to determine the size.




## -remarks



Use this structure to access the AudioSpecificConfig() data that follows an <a href="https://docs.microsoft.com/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo">HEAACWAVEINFO</a> structure. This data is present only when the <b>wStructType</b> member of the <b>HEAACWAVEFORMAT</b> structure is zero.



