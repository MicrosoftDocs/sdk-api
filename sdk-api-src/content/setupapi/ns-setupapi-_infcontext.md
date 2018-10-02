---
UID: NS:setupapi._INFCONTEXT
title: "_INFCONTEXT"
author: windows-sdk-content
description: The INFCONTEXT structure stores context information that functions such as SetupGetLineText use to navigate INF files.
old-location: setup\infcontext_str.htm
tech.root: SetupApi
ms.assetid: 5b3d32a8-e651-4017-aaa7-b532ec47da53
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PINFCONTEXT, INFCONTEXT, INFCONTEXT structure [Setup API], PINFCONTEXT, PINFCONTEXT structure pointer [Setup API], _INFCONTEXT, _setupapi_infcontext_str, setup.infcontext_str, setupapi/INFCONTEXT, setupapi/PINFCONTEXT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: setupapi.h
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
 - Setupapi.h
api_name:
 - INFCONTEXT
product: Windows
targetos: Windows
req.typenames: INFCONTEXT, *PINFCONTEXT
req.redist: 
---

# _INFCONTEXT structure


## -description


The 
<b>INFCONTEXT</b> structure stores context information that functions such as 
<a href="https://msdn.microsoft.com/ab689e03-5f4f-4f06-bd44-a927e1ab702d">SetupGetLineText</a> use to navigate INF files.


## -struct-fields




### -field Inf

Handle to the INF file returned by 
<a href="https://msdn.microsoft.com/a0f29f2c-2ac8-4f2d-adad-7a948d5a4eb7">SetupOpenInfFile</a>.


### -field CurrentInf

Pointer to the current INF file. The <b>Inf</b> member may point to multiple files if they were appended to the open INF file using 
<a href="https://msdn.microsoft.com/12b1c676-912f-4876-998c-6b0ff162b95d">SetupOpenAppendInfFile</a>.


### -field Section

Section in the current INF file.


### -field Line

Line of the current section in the INF file. 




<div class="alert"><b>Note</b>    The setup functions use this structure internally and it must not be accessed or modified by applications. It is included here for informational purposes only.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/ff4b13b6-62ca-48ae-9ddd-e721bde7bd8b">SetupFindFirstLine</a>



<a href="https://msdn.microsoft.com/ba5b3c62-c6b7-4ec1-83e2-45cdc910a34d">SetupFindNextLine</a>



<a href="https://msdn.microsoft.com/c08e22d0-7eb3-4fad-82a6-e9d4f50c4e73">SetupFindNextMatchLine</a>



<a href="https://msdn.microsoft.com/837F1864-CE2F-4A9A-A7D9-18EB8622541E">Structures</a>
 

 

