---
UID: NF:objbase.CoFileTimeNow
title: CoFileTimeNow function (objbase.h)
description: Returns the current time as a FILETIME structure.
helpviewer_keywords: ["CoFileTimeNow","CoFileTimeNow function [COM]","_com_CoFileTimeNow","com.cofiletimenow","combaseapi/CoFileTimeNow"]
old-location: com\cofiletimenow.htm
tech.root: com
ms.assetid: 00083429-1d61-4a0b-bb73-82158869466d
ms.date: 12/05/2018
ms.keywords: CoFileTimeNow, CoFileTimeNow function [COM], _com_CoFileTimeNow, com.cofiletimenow, combaseapi/CoFileTimeNow
f1_keywords:
- objbase/CoFileTimeNow
dev_langs:
- c++
req.header: objbase.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ole32.dll
- API-MS-Win-OLE32-IE-l1-1-0.dll
- ole32_wp.dll
api_name:
- CoFileTimeNow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CoFileTimeNow function


## -description


Returns the current time as a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters




### -param lpFileTime [out]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that receives the current time.


## -returns



This function returns S_OK to indicate success.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-codosdatetimetofiletime">CoDosDateTimeToFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cofiletimetodosdatetime">CoFileTimeToDosDateTime</a>
 

 

