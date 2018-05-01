---
UID: NF:wmsdkidl.IWMSyncReader.GetMaxStreamSampleSize
title: IWMSyncReader::GetMaxStreamSampleSize method
author: windows-driver-content
description: The GetMaxStreamSampleSize method retrieves the maximum sample size for a specified stream in the file that is open in the synchronous reader.
old-location: wmformat\iwmsyncreader_getmaxstreamsamplesize.htm
old-project: wmformat
ms.assetid: 8b098985-4eb2-4292-a9b9-cfdd051e9c0e
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetMaxStreamSampleSize method [windows Media Format], GetMaxStreamSampleSize method [windows Media Format], IWMSyncReader interface, GetMaxStreamSampleSize,IWMSyncReader.GetMaxStreamSampleSize, IWMSyncReader, IWMSyncReader interface [windows Media Format], GetMaxStreamSampleSize method, IWMSyncReader::GetMaxStreamSampleSize, IWMSyncReaderGetMaxStreamSampleSize, wmformat.iwmsyncreader_getmaxstreamsamplesize, wmsdkidl/IWMSyncReader::GetMaxStreamSampleSize
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
-	IWMSyncReader.GetMaxStreamSampleSize
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::GetMaxStreamSampleSize method


## -description



The <b>GetMaxStreamSampleSize</b> method retrieves the maximum sample size for a specified stream in the file that is open in the synchronous reader.




## -parameters




### -param wStream [in]

<b>WORD</b> containing the stream number for which you want to retrieve the maximum sample size.


### -param pcbMax [out]

Pointer to a <b>DWORD</b> value that receives the maximum sample size, in bytes, for the stream specified in <i>wStream</i>.


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
<i>pcbMax</i> is <b>NULL</b>.

OR

<i>wStream</i> specifies an invalid stream number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
No file is open in the synchronous reader.

</td>
</tr>
</table>
 




## -remarks



This method retrieves the maximum sample size for an individual stream. The stream may be one of several in an output. If you are using output numbers, you should use <a href="https://msdn.microsoft.com/84fbc2c7-001b-4339-a7df-89914274a72b">IWMSyncReader::GetMaxOutputSampleSize</a> to retrieve the maximum sample size for the entire output.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>
 

 

