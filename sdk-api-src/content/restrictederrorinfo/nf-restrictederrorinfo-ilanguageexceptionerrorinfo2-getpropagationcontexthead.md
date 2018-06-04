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

# ILanguageExceptionErrorInfo2::GetPropagationContextHead


## -description


Retrieves the propagation context head.


## -parameters




### -param propagatedLanguageExceptionErrorInfoHead [out]

On success, returns an <a href="https://msdn.microsoft.com/A943EE85-F2A9-4D5E-AA6F-0C4AB8556A4C">ILanguageExceptionErrorInfo2</a> object that represents the head of the propagation context.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use <b>GetPropagationContextHead</b> to retrieve the linked list of <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> objects that contains additional error information on the exception in question. You can then use <a href="https://msdn.microsoft.com/10A45EF1-AF8F-498D-B95B-FCE9EF8AB203">GetPreviousLanguageExceptionErrorInfo</a> to move through that linked list, and examine each error separately.

 The operating system also uses this method to retrieve the stored exceptions associated with the error.




## -see-also




<a href="https://msdn.microsoft.com/A943EE85-F2A9-4D5E-AA6F-0C4AB8556A4C">ILanguageExceptionErrorInfo2</a>
 

 

