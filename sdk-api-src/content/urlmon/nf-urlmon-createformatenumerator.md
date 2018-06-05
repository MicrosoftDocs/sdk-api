---
UID: NF:urlmon.CreateFormatEnumerator
title: CreateFormatEnumerator function
author: windows-sdk-content
description: Creates an object that implements IEnumFORMATETC over a static array of FORMATETC structures.
old-location: com\createformatenumerator.htm
old-project: com
ms.assetid: 302418e5-48b6-46ee-bb96-2a8170c4af5e
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CreateFormatEnumerator, CreateFormatEnumerator function [COM], _ole_CreateFormatEnumerator, com.createformatenumerator, urlmon/CreateFormatEnumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: urlmon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Urlmon.dll
api_name:
-	CreateFormatEnumerator
product: Windows
targetos: Windows
req.lib: Urlmon.lib
req.dll: Urlmon.dll
req.irql: 
req.product: Windows UI
---

# CreateFormatEnumerator function


## -description


Creates an object that implements <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> over a static array of <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures.


## -parameters




### -param cfmtetc [in]

Number of <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures in the static array specified by the <i>rgfmtetc</i> parameter. The <i>cfmtetc</i> parameter cannot be zero.


### -param rgfmtetc [in]

Pointer to a static array of <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures.


### -param ppenumfmtetc [out]

Address of <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> pointer variable that receives the interface pointer to the enumerator object.


## -returns



This function returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



The <b>CreateFormatEnumerator</b> function creates an enumerator object that implements <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> over a static array of <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures. The <i>cfmtetc</i> parameter specifies the number of these structures. With the pointer, you can call the standard enumeration methods to enumerate the structures.



