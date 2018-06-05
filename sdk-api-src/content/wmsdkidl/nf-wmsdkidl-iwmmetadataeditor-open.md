---
UID: NF:wmsdkidl.IWMMetadataEditor.Open
title: IWMMetadataEditor::Open
author: windows-sdk-content
description: The Open method opens an ASF file.
old-location: wmformat\iwmmetadataeditor_open.htm
old-project: wmformat
ms.assetid: 01dd09ff-35d2-4e00-9eab-5110a426449f
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMMetadataEditor interface [windows Media Format],Open method, IWMMetadataEditor.Open, IWMMetadataEditor::Open, IWMMetadataEditorOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMMetadataEditor interface, wmformat.iwmmetadataeditor_open, wmsdkidl/IWMMetadataEditor::Open
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMMetadataEditor.Open
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMMetadataEditor::Open


## -description



The <b>Open</b> method opens an ASF file.




## -parameters




### -param pwszFilename [in]

Pointer to a wide-character <b>null</b>-terminated string containing the file name.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_FILE_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The method failed to open the specified file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszFilename</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ad19cd3e-d1ef-4d6c-ac23-29a56e5c1d66">IWMMetadataEditor Interface</a>



<a href="https://msdn.microsoft.com/e35f5f85-659e-4a1f-8bfd-4ad3e946d733">IWMMetadataEditor2::OpenEx</a>



<a href="https://msdn.microsoft.com/7c10d0ea-8a19-4374-94f2-e12d7c1ba553">IWMMetadataEditor::Close</a>
 

 

