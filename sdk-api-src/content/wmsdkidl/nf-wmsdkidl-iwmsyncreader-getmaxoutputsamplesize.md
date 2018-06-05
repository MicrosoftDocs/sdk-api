---
UID: NF:wmsdkidl.IWMSyncReader.GetMaxOutputSampleSize
title: IWMSyncReader::GetMaxOutputSampleSize
author: windows-sdk-content
description: The GetMaxOutputSampleSize method retrieves the maximum sample size for a specified output of the file open in the synchronous reader.
old-location: wmformat\iwmsyncreader_getmaxoutputsamplesize.htm
old-project: wmformat
ms.assetid: 84fbc2c7-001b-4339-a7df-89914274a72b
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetMaxOutputSampleSize, GetMaxOutputSampleSize method [windows Media Format], GetMaxOutputSampleSize method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetMaxOutputSampleSize method, IWMSyncReader.GetMaxOutputSampleSize, IWMSyncReader::GetMaxOutputSampleSize, IWMSyncReaderGetMaxOutputSampleSize, wmformat.iwmsyncreader_getmaxoutputsamplesize, wmsdkidl/IWMSyncReader::GetMaxOutputSampleSize
ms.prod: windows
ms.technology: windows-sdk
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
-	IWMSyncReader.GetMaxOutputSampleSize
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::GetMaxOutputSampleSize


## -description



The <b>GetMaxOutputSampleSize</b> method retrieves the maximum sample size for a specified output of the file open in the synchronous reader.




## -parameters




### -param dwOutput [in]

<b>DWORD</b> containing the output number for which you want to retrieve the maximum sample size.


### -param pcbMax [out]

Pointer to a <b>DWORD</b> value that receives the maximum sample size, in bytes, for the output specified in <i>dwOutput</i>.


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

<i>dwOutput</i> specifies an invalid output number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
No file is opened in the synchronous reader.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NOT_CONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
The specified output is not currently configured for playback.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The synchronous reader failed to initialize an internal object.

</td>
</tr>
</table>
 




## -remarks



In some scenarios, such as multiple bit rate streaming, the output encompasses several streams. The size returned is the maximum sample size for all of the streams associated with the specified output.

You can retrieve the maximum sample size for a specific stream by using <a href="https://msdn.microsoft.com/8b098985-4eb2-4292-a9b9-cfdd051e9c0e">IWMSyncReader::GetMaxStreamSampleSize</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>
 

 

