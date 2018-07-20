---
UID: NF:ole.OleSaveToStream
title: OleSaveToStream function
author: windows-sdk-content
description: Saves an object with the IPersistStream interface on it to the specified stream.
old-location: com\olesavetostream.htm
old-project: com
ms.assetid: 0085c6a8-1a94-4379-9937-c8d792d130da
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: OleSaveToStream, OleSaveToStream function [COM], _ole_OleSaveToStream, com.olesavetostream, ole/OleSaveToStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole.h
req.include-header: Ole2.h
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
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleSaveToStream
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# OleSaveToStream function


## -description


Saves an object with the <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> interface on it to the specified stream.


## -parameters




### -param

TBD




#### - pPStm [in]

Pointer to the <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> interface on the object to be saved to the stream. The <i>pPStm</i> parameter cannot be <b>NULL</b>.


#### - pStm [in]

 Pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface on the stream in which the object is to be saved.


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
<dt><b>STGMEDIUM_E_FULL</b></dt>
</dl>
</td>
<td width="60%">
The object could not be saved due to lack of disk space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPStm</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 

This function can also return any of the error values returned by the <a href="https://msdn.microsoft.com/c08bfbc8-f7ac-4534-8c98-c732c6daa2f7">WriteClassStm</a> function or the <a href="https://msdn.microsoft.com/b748b4f9-ef9c-486b-bdc4-4d23c4640ff7">IPersistStream::Save</a> method.




## -remarks



This function simplifies saving an object that implements the <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a> interface to a stream. In this stream, the object's CLSID precedes its data. When the stream is retrieved, the CLSID permits the proper code to be associated with the data. The <b>OleSaveToStream</b> function does the following:

<ul>
<li>Calls the <a href="https://msdn.microsoft.com/921a3b86-a240-454e-9411-8d653e02b90e">IPersist::GetClassID</a> method to get the object's CLSID.</li>
<li>Writes the CLSID to the stream with the <a href="https://msdn.microsoft.com/c08bfbc8-f7ac-4534-8c98-c732c6daa2f7">WriteClassStm</a> function.</li>
<li>Calls the <a href="https://msdn.microsoft.com/b748b4f9-ef9c-486b-bdc4-4d23c4640ff7">IPersistStream::Save</a> method with <i>fClearDirty</i> set to <b>TRUE</b>, which clears the dirty bit in the object.</li>
</ul>
The companion helper, <a href="https://msdn.microsoft.com/2d54a0ef-906b-4886-a095-4ff2f3d4e634">OleLoadFromStream</a>, loads objects saved in this way.




## -see-also




<a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>



<a href="https://msdn.microsoft.com/2d54a0ef-906b-4886-a095-4ff2f3d4e634">OleLoadFromStream</a>
 

 

