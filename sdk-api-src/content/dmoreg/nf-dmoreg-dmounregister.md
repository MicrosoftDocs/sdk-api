---
UID: NF:dmoreg.DMOUnregister
title: DMOUnregister function
author: windows-sdk-content
description: The DMOUnregister function unregisters a DMO.
old-location: dshow\dmounregister.htm
old-project: DirectShow
ms.assetid: 7f65789d-7654-4da2-a572-e07c1e81b4ae
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DMOUnregister, DMOUnregister function [DirectShow], dmoreg/DMOUnregister, dshow.dmounregister
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dmoreg.h
req.include-header: Dmo.h
req.target-type: Windows
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdmo.dll
api_name:
-	DMOUnregister
product: Windows
targetos: Windows
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
---

# DMOUnregister function


## -description


The DMOUnregister function unregisters a DMO.


## -parameters




### -param clsidDMO

Class identifier (CLSID) of the DMO.


### -param guidCategory

GUID that specifies the category from which to remove the DMO. Use GUID_NULL to unregister the DMO from every category. See <a href="https://msdn.microsoft.com/d67debd0-8ecb-41ab-bc6c-b27cba97c65a">DMO GUIDs</a> for a list of category GUIDs.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Result Code</th>
<th>Description</th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>Invalid argument</td>
</tr>
<tr>
<td>S_FALSE</td>
<td>This CLSID was not registered in the specified category.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0a380dc0-23f0-4ef0-898a-3b5afddf5eaa">DMO Functions</a>
 

 

