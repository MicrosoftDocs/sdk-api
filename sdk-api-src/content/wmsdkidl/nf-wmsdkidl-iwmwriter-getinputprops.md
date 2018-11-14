---
UID: NF:wmsdkidl.IWMWriter.GetInputProps
title: IWMWriter::GetInputProps
author: windows-sdk-content
description: The GetInputProps method retrieves the current media properties of a specified input stream.
old-location: wmformat\iwmwriter_getinputprops.htm
tech.root: wmformat
ms.assetid: 2889a1a7-3111-4c13-b15a-659f519c22f6
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetInputProps, GetInputProps method [windows Media Format], GetInputProps method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],GetInputProps method, IWMWriter.GetInputProps, IWMWriter::GetInputProps, IWMWriterGetInputProps, wmformat.iwmwriter_getinputprops, wmsdkidl/IWMWriter::GetInputProps
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
 - IWMWriter.GetInputProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMWriter.GetInputProps
: 
---

# IWMWriter::GetInputProps


## -description



The <b>GetInputProps</b> method retrieves the current media properties of a specified input stream.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input index number.


### -param ppInput [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/d901ac66-d4b3-4256-bd7b-53cccb3de644">IWMInputMediaProps</a> object.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwInputNum</i> value is greater than the highest index number.

</td>
</tr>
</table>
 




## -remarks



The range of indexes to use for the <i>dwInputNum</i> parameter can be found by calling <a href="https://msdn.microsoft.com/0cb3cd79-0640-4a3b-8e8b-d81df2ff749f">GetInputCount</a>.

Manipulating the <b>IWMInputMediaProps</b> object has no effect on the writer, unless the application calls the <a href="https://msdn.microsoft.com/15084a4d-06e8-4f74-9697-ced794d2cdae">SetInputProps</a> method to configure the input.




## -see-also




<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/f468f74d-7eed-4819-957d-241903f44d2d">To Identify Inputs By Number</a>
 

 

