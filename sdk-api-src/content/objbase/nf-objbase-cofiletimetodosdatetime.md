---
UID: NF:objbase.CoFileTimeToDosDateTime
title: CoFileTimeToDosDateTime function (objbase.h)
description: Converts a FILETIME into MS-DOS date and time values.
helpviewer_keywords: ["CoFileTimeToDosDateTime","CoFileTimeToDosDateTime function [COM]","_com_CoFileTimeToDosDateTime","com.cofiletimetodosdatetime","objbase/CoFileTimeToDosDateTime"]
old-location: com\cofiletimetodosdatetime.htm
tech.root: com
ms.assetid: 38670fe7-10cf-44e2-a5f1-60ec43fd83b5
ms.date: 12/05/2018
ms.keywords: CoFileTimeToDosDateTime, CoFileTimeToDosDateTime function [COM], _com_CoFileTimeToDosDateTime, com.cofiletimetodosdatetime, objbase/CoFileTimeToDosDateTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoFileTimeToDosDateTime
 - objbase/CoFileTimeToDosDateTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - Ole32.dll
api_name:
 - CoFileTimeToDosDateTime
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# CoFileTimeToDosDateTime function


## -description

Converts a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> into MS-DOS date and time values.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters

### -param lpFileTime [in]

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

### -param lpDosDate [out]

Receives the MS-DOS date.

### -param lpDosTime [out]

Receives the MS-DOS time.

## -returns

If the function succeeds, the return value is <b>TRUE</b>; otherwise, it is <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-codosdatetimetofiletime">CoDosDateTimeToFileTime</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cofiletimenow">CoFileTimeNow</a>
