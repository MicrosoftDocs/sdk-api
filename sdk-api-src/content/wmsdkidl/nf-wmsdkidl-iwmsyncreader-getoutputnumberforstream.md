---
UID: NF:wmsdkidl.IWMSyncReader.GetOutputNumberForStream
title: IWMSyncReader::GetOutputNumberForStream
author: windows-driver-content
description: The GetOutputNumberForStream method retrieves the output number that corresponds with the specified stream.
old-location: wmformat\iwmsyncreader_getoutputnumberforstream.htm
old-project: wmformat
ms.assetid: 605f5a66-aa06-4d4e-998e-1a3f7d1c7be6
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetOutputNumberForStream, GetOutputNumberForStream method [windows Media Format], GetOutputNumberForStream method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetOutputNumberForStream method, IWMSyncReader.GetOutputNumberForStream, IWMSyncReader::GetOutputNumberForStream, IWMSyncReaderGetOutputNumberForStream, wmformat.iwmsyncreader_getoutputnumberforstream, wmsdkidl/IWMSyncReader::GetOutputNumberForStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
-	IWMSyncReader.GetOutputNumberForStream
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::GetOutputNumberForStream


## -description



The <b>GetOutputNumberForStream</b> method retrieves the output number that corresponds with the specified stream.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which you want to retrieve the corresponding output number.


### -param pdwOutputNum [out]

Pointer to a <b>DWORD</b> that will receive the output number that corresponds to the stream number specified in <i>wStreamNum</i>.


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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> specifies an invalid stream number.

</td>
</tr>
</table>
 




## -remarks



More than one stream can be encompassed by an output, as in the case of multiple bit rate files.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>
 

 

