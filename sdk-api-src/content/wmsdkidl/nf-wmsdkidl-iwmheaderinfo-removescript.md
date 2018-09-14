---
UID: NF:wmsdkidl.IWMHeaderInfo.RemoveScript
title: IWMHeaderInfo::RemoveScript
author: windows-sdk-content
description: The RemoveScript method enables the object to remove a script from the header section of the ASF file.
old-location: wmformat\iwmheaderinfo_removescript.htm
tech.root: wmformat
ms.assetid: c66e808d-25f9-4745-8bcc-731f2556f470
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMHeaderInfo interface [windows Media Format],RemoveScript method, IWMHeaderInfo.RemoveScript, IWMHeaderInfo::RemoveScript, IWMHeaderInfoRemoveScript, RemoveScript, RemoveScript method [windows Media Format], RemoveScript method [windows Media Format],IWMHeaderInfo interface, wmformat.iwmheaderinfo_removescript, wmsdkidl/IWMHeaderInfo::RemoveScript
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMHeaderInfo.RemoveScript
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMHeaderInfo::RemoveScript


## -description



The <b>RemoveScript</b> method enables the object to remove a script from the header section of the ASF file.




## -parameters




### -param wIndex [in]

<b>WORD</b> containing the index of the script.


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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object cannot be currently configured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



The writer only supports this method before the <b>BeginWriting</b> method has been called. This method is not supported by the reader.




## -see-also




<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/e20644fb-077e-4eee-8802-6099002f3969">IWMHeaderInfo::AddScript</a>



<a href="https://msdn.microsoft.com/779a7618-9f22-4caf-8a4e-b622e422c30d">IWMHeaderInfo::GetScript</a>
 

 

