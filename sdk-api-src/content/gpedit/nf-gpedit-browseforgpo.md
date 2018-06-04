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

# BrowseForGPO function


## -description


The
    <b>BrowseForGPO</b> function creates a GPO browser dialog box that allows the user to open or create a GPO.


## -parameters




### -param lpBrowseInfo [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/a0d038f2-66f1-4a79-b9e7-189cb57b80a9">GPOBROWSEINFO</a> structure that contains information used to initialize the dialog box. When 
the <b>BrowseForGPO</b> function returns, this structure contains information about the user's actions.


## -returns



If the function succeeds, the return value is <b>S_OK</b>. If the user cancels or closes the dialog box, the return value is <b>HRESULT_FROM_WIN32</b>(<b>ERROR_CANCELLED</b>). Otherwise, the function returns one of the COM error codes defined in the header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/a0d038f2-66f1-4a79-b9e7-189cb57b80a9">GPOBROWSEINFO</a>



<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>
 

 

