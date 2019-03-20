---
UID: NF:wmsdkidl.IWMMetadataEditor.Open
title: IWMMetadataEditor::Open (wmsdkidl.h)
author: windows-sdk-content
description: The Open method opens an ASF file.
old-location: wmformat\iwmmetadataeditor_open.htm
tech.root: wmformat
ms.assetid: 01dd09ff-35d2-4e00-9eab-5110a426449f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMMetadataEditor interface [windows Media Format],Open method, IWMMetadataEditor.Open, IWMMetadataEditor::Open, IWMMetadataEditorOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMMetadataEditor interface, wmformat.iwmmetadataeditor_open, wmsdkidl/IWMMetadataEditor::Open
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMMetadataEditor.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Dd757232(v=VS.85).aspx">IWMMetadataEditor Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757234(v=VS.85).aspx">IWMMetadataEditor2::OpenEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757235(v=VS.85).aspx">IWMMetadataEditor::Close</a>
 

 

