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

# IInstallationAgent::RecordInstallationResult


## -description


Records the result for an update. The result is specified by an <a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a> object.


## -parameters




### -param installationResultCookie [in]

A string value that identifies the result cookie.


### -param hresult [in]

The identifier of the result.


### -param extendedReportingData [in]

An <a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a> interface that represents a collection of strings that contain the result for an update.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 




## -see-also




<a href="https://msdn.microsoft.com/B24B527C-D92B-4BEB-ADCC-5E2BA684A478">IInstallationAgent</a>
 

 

