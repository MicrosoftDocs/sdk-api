---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WdsCliGetDriverQueryXml function


## -description


This function generates an XML string which can be used to query a WDS server for driver packages using the <a href="https://msdn.microsoft.com/C9AA3036-8E34-4F57-829C-F5D8CDA2EAA7">WdsCliObtainDriverPackagesEx</a> function.  The target OS information section of the WDS driver query XML is generated if the path to the Windows directory of the applied image is specified. 


## -parameters




### -param pwszWinDirPath [in, optional]

The path to the Windows directory of the applied image. This parameter is optional. If it is specified,  the section of the WDS driver query XML  for the target operating system is generated.


### -param ppwszDriverQuery [out]

A pointer to a pointer to a string that receives the generated WDS driver query XML. The caller has to free this buffer using "delete[](*ppwszDriverQuery)".


## -returns



If the function succeeds, the return is <b>S_OK</b>.



