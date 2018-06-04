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

# PTOpenProviderEx function


## -description


Opens an instance of a print ticket provider.


## -parameters




### -param pszPrinterName [in]

A pointer to the full name of a print queue.


### -param dwMaxVersion

TBD


### -param dwPrefVersion

TBD


### -param phProvider [out]

A pointer to a handle for the provider.


### -param pUsedVersion

TBD




#### - maxVersion

The latest version of the <a href="https://msdn.microsoft.com/98d5f8ec-54bd-4e88-b632-ed427b599cb6">Print Schema</a> that the caller supports.


#### - prefVersion

The version of the Print Schema requested by the caller.


#### - usedVersion [out]

A pointer to the version of the Print Schema that the print ticket provider will use.


## -returns



If the operation succeeds, the return value is S_OK, otherwise the <b>HRESULT</b> contains an error code.

For more information about COM error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>.




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>

        The <i>pszPrinterName</i> parameter must be the full name, not the truncated name as it may appear in a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>.

The first version of the Print Schema was released with Windows Vista and is version 1. If the print ticket provider does not support <i>prefVersion</i>, <b>PTOpenProviderEx</b> successfully opens a handle and returns an earlier version in <i>usedVersion</i>.

To avoid a resource leak, <i>phProvider</i> must be closed with <a href="https://msdn.microsoft.com/28e85b53-fd0c-4210-ae2b-794efaf65bd4">PTCloseProvider</a>.




## -see-also




<a href="https://msdn.microsoft.com/98d5f8ec-54bd-4e88-b632-ed427b599cb6">Print Schema</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

