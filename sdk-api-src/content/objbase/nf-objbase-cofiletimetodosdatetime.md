---
UID: NF:objbase.CoFileTimeToDosDateTime
title: CoFileTimeToDosDateTime function (objbase.h)
author: windows-sdk-content
description: Converts a FILETIME into MS-DOS date and time values.
old-location: com\cofiletimetodosdatetime.htm
tech.root: com
ms.assetid: 38670fe7-10cf-44e2-a5f1-60ec43fd83b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoFileTimeToDosDateTime, CoFileTimeToDosDateTime function [COM], _com_CoFileTimeToDosDateTime, com.cofiletimetodosdatetime, objbase/CoFileTimeToDosDateTime
ms.topic: function
f1_keywords: 
 - "objbase/CoFileTimeToDosDateTime"
dev_langs:
 - c++
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - CoFileTimeToDosDateTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CoFileTimeToDosDateTime function


## -description


Converts a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> into MS-DOS date and time values.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters




### -param lpFileTime [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.


### -param lpDosDate [out]

Receives the MS-DOS date.


### -param lpDosTime [out]

Receives the MS-DOS time.


## -returns



If the function succeeds, the return value is <b>TRUE</b>; otherwise, it is <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-codosdatetimetofiletime">CoDosDateTimeToFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cofiletimenow">CoFileTimeNow</a>
 

 

