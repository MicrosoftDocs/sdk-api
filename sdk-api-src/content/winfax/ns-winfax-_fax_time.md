---
UID: NS:winfax._FAX_TIME
title: "_FAX_TIME"
author: windows-sdk-content
description: The FAX_TIME structure represents a time, using individual members for the current hour and minute. The time is expressed in Coordinated Universal Time (UTC).
old-location: fax\_mfax_fax_time_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_24fm.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PFAX_TIME, FAX_TIME, FAX_TIME structure [Fax Service], FAX_TIMEA, FAX_TIMEW, PFAX_TIME, PFAX_TIME structure pointer [Fax Service], _FAX_TIME, _mfax_fax_time_str, fax._mfax_fax_time_str, winfax/FAX_TIME, winfax/FAX_TIMEA, winfax/FAX_TIMEW, winfax/PFAX_TIME"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_TIMEW (Unicode) and FAX_TIMEA (ANSI)
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
 - Winfax.h
api_name:
 - FAX_TIME
 - FAX_TIMEA
 - FAX_TIMEW
product: Windows
targetos: Windows
req.typenames: FAX_TIME, *PFAX_TIME
req.redist: 
---

# _FAX_TIME structure


## -description


The <b>FAX_TIME</b> structure represents a time, using individual members for the current hour and minute. The time is expressed in Coordinated Universal Time (UTC).


## -struct-fields




### -field Hour

Type: <b>WORD</b>

Specifies a 16-bit unsigned integer that is the current hour. Valid values are 0 through 23.


### -field Minute

Type: <b>WORD</b>

Specifies a 16-bit unsigned integer that is the current minute. Valid values are 0 through 59.


## -remarks



The <a href="https://msdn.microsoft.com/94b09265-a53c-47a2-8b24-bccb662b21c6">FAX_CONFIGURATION</a> structure includes a <b>FAX_TIME</b> structure to describe the discount period that applies when a fax server is sending fax transmissions. 




## -see-also




<a href="https://msdn.microsoft.com/94b09265-a53c-47a2-8b24-bccb662b21c6">FAX_CONFIGURATION</a>



<a href="https://msdn.microsoft.com/be81e221-4aba-4c63-9640-337bee49fdb4">Fax Service Client API Structures</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/c29f0eaf-39a5-45e2-afb9-010494552969">FaxGetConfiguration</a>



<a href="https://msdn.microsoft.com/e99d5254-4008-411a-ae56-8b0cbe7a4933">FaxSetConfiguration</a>
 

 

