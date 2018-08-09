---
UID: NF:wmsdkidl.WMCreateEditor
title: WMCreateEditor function
author: windows-sdk-content
description: The WMCreateEditor function creates a metadata editor object.
old-location: wmformat\wmcreateeditor.htm
old-project: wmformat
ms.assetid: 3eed88d5-18e9-40b4-998d-af33ac5440b2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WMCreateEditor, WMCreateEditor function [windows Media Format], wmformat.wmcreateeditor, wmsdkidl/WMCreateEditor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateEditor
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMCreateEditor function


## -description



The <b>WMCreateEditor</b> function creates a metadata editor object.




## -parameters




### -param ppEditor [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/ad19cd3e-d1ef-4d6c-ac23-29a56e5c1d66">IWMMetadataEditor</a> interface of the newly created metadata editor object.


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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/224eea1c-1d0d-47ac-9d99-c13674284f6d">Metadata Editor Object</a>
 

 

