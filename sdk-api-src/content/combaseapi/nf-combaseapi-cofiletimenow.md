---
UID: NF:combaseapi.CoFileTimeNow
title: CoFileTimeNow function (combaseapi.h)
description: The CoFileTimeNow function (combaseapi.h) returns the current time as a FILETIME structure.
helpviewer_keywords: ["CoFileTimeNow","CoFileTimeNow function [COM]","_com_CoFileTimeNow","com.cofiletimenow","combaseapi/CoFileTimeNow"]
old-location: com\cofiletimenow.htm
tech.root: com
ms.assetid: 00083429-1d61-4a0b-bb73-82158869466d
ms.date: 08/10/2022
ms.keywords: CoFileTimeNow, CoFileTimeNow function [COM], _com_CoFileTimeNow, com.cofiletimenow, combaseapi/CoFileTimeNow
req.header: combaseapi.h
req.include-header: Objbase.h
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
 - CoFileTimeNow
 - combaseapi/CoFileTimeNow
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
 - ext-ms-win-com-ole32-l1-1-5.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-OLE32-IE-l1-1-0.dll
 - ole32_wp.dll
api_name:
 - CoFileTimeNow
---

# CoFileTimeNow function


## -description

Returns the current time as a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters

### -param lpFileTime [out]

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the current time.

## -returns

This function returns S_OK to indicate success.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-codosdatetimetofiletime">CoDosDateTimeToFileTime</a>



<a href="/windows/desktop/api/objbase/nf-objbase-cofiletimetodosdatetime">CoFileTimeToDosDateTime</a>
