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

# SHAddFromPropSheetExtArray function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Adds pages to a property sheet extension array created by <a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>.


## -parameters




### -param hpsxa [in]

Type: <b>HPSXA</b>

The array of property sheet handlers returned by <a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>.


### -param lpfnAddPage [in]

Type: <b>LPFNADDPROPSHEETPAGE</b>

A pointer to an <a href="https://msdn.microsoft.com/37673813-89dc-4624-a58b-fe5f44df46c6">AddPropSheetPageProc</a> callback function. It is called once for each property sheet handler. The callback function then returns the information needed to add a page to the handler's property sheet.


### -param lParam

Type: <b>LPARAM</b>

A pointer to application-defined data. This data is passed to the callback function specified by <i>lpfnAddPage</i>.


## -returns



Type: <b>UINT</b>

Returns the number of pages actually added.




## -remarks



This function should be called only once for the property sheet extension array named in <i>hpsxa</i>.

This function calls each extension's <a href="https://msdn.microsoft.com/76a2a94b-b79f-41d1-9e42-fbfda545d12f">IShellPropSheetExt::AddPages</a> method. See that page for further details.




## -see-also




<a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>



<a href="https://msdn.microsoft.com/beb3c1b1-deef-440d-8cf7-f76b3f396efa">SHDestroyPropSheetExtArray</a>



<a href="https://msdn.microsoft.com/a8bdde44-d668-46c4-9e58-7a45b775fe09">SHReplaceFromPropSheetExtArray</a>
 

 

