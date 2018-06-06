---
UID: NF:ole2.OleQueryCreateFromData
title: OleQueryCreateFromData function
author: windows-sdk-content
description: Checks whether a data object has one of the formats that would allow it to become an embedded object through a call to either the OleCreateFromData or OleCreateStaticFromData function.
old-location: com\olequerycreatefromdata.htm
old-project: com
ms.assetid: 58fffb8c-9726-4801-84ce-6fb670b865c8
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: OleQueryCreateFromData, OleQueryCreateFromData function [COM], _ole_OleQueryCreateFromData, com.olequerycreatefromdata, ole2/OleQueryCreateFromData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
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
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-Com-OLE32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleQueryCreateFromData
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleQueryCreateFromData function


## -description


Checks whether a data object has one of the formats that would allow it to become an embedded object through a call to either the <a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a> or <a href="https://msdn.microsoft.com/847d82f5-149d-48a4-a228-f5551a07a790">OleCreateStaticFromData</a> function.


## -parameters




### -param pSrcDataObject [in]

Pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data transfer object to be queried.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No formats are present that support either embedded- or static-object creation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_S_STATIC</b></dt>
</dl>
</td>
<td width="60%">
Formats that support static-object creation are present.

</td>
</tr>
</table>
 




## -remarks



When an application retrieves a data transfer object through a call to the <a href="https://msdn.microsoft.com/c5e7badb-339b-48d5-8c9a-3950e2ffe6bf">OleGetClipboard</a> function, the application should call <b>OleQueryCreateFromData</b> as part of the process of deciding to enable or disable the <b>Edit/Paste</b> or <b>Edit/Paste Special...</b> commands. It tests for the presence of the following formats in the data object:

<ul>
<li>CF_EMBEDDEDOBJECT</li>
<li>CF_EMBEDSOURCE</li>
<li>cfFileName</li>
<li>CF_METAFILEPICT</li>
<li>CF_DIB</li>
<li>CF_BITMAP</li>
<li>CF_ENHMETAFILE</li>
</ul>
Determining that the data object has one of these formats does not absolutely guarantee that the object creation will succeed, but is intended to help the process.

If <b>OleQueryCreateFromData</b> finds one of the CF_METAFILEPICT, CF_BITMAP,  CF_DIB, or CF_ENHMETAFILE formats and none of the other formats, it returns OLE_S_STATIC, indicating that you should call the <a href="https://msdn.microsoft.com/847d82f5-149d-48a4-a228-f5551a07a790">OleCreateStaticFromData</a> function to create the embedded object.

If <b>OleQueryCreateFromData</b> finds one of the other formats (CF_EMBEDDEDOBJECT, CF_EMBEDSOURCE, or cfFileName), even in combination with the static formats, it returns S_OK, indicating that you should call the <a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a> function to create the embedded object. 





## -see-also




<a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a>



<a href="https://msdn.microsoft.com/847d82f5-149d-48a4-a228-f5551a07a790">OleCreateStaticFromData</a>



<a href="https://msdn.microsoft.com/9ebdcd7f-06c1-4464-a66c-4d134a6b5d36">OleQueryLinkFromData</a>
 

 

