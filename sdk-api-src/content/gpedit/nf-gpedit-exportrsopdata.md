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

# ExportRSoPData function


## -description


The
    <b>ExportRSoPData</b> function exports a WMI namespace that contains RSoP information to a data file. The function writes the information to a data file that can be imported to a WMI namespace with a call to the 
<a href="https://msdn.microsoft.com/d3b4ef2e-a828-445a-83de-d5c9e4a4d98b">ImportRSoPData</a> function.


## -parameters




### -param lpNameSpace [in]

A pointer to a string that specifies the namespace which contains the RSoP data.


### -param lpFileName [in]

A pointer to a string that specifies the name of the file to receive the RSoP data.


## -returns



If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the header file WinError.h.




## -remarks



It is recommended that you call the 
<b>ExportRSoPData</b> function twice: one time to process the user data and a second time to process the computer data.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/d3b4ef2e-a828-445a-83de-d5c9e4a4d98b">ImportRSoPData</a>
 

 

