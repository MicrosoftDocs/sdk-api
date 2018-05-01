---
UID: NF:wmsdkidl.IWMWriterAdvanced3.GetStatisticsEx
title: IWMWriterAdvanced3::GetStatisticsEx method
author: windows-driver-content
description: The GetStatisticsEx method retrieves extended statistics for the writer.
old-location: wmformat\iwmwriteradvanced3_getstatisticsex.htm
old-project: wmformat
ms.assetid: 3ea41491-409c-42b7-a4b2-f0d7c222c299
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetStatisticsEx method [windows Media Format], GetStatisticsEx method [windows Media Format], IWMWriterAdvanced3 interface, GetStatisticsEx,IWMWriterAdvanced3.GetStatisticsEx, IWMWriterAdvanced3, IWMWriterAdvanced3 interface [windows Media Format], GetStatisticsEx method, IWMWriterAdvanced3::GetStatisticsEx, IWMWriterAdvanced3GetStatisticsEx, wmformat.iwmwriteradvanced3_getstatisticsex, wmsdkidl/IWMWriterAdvanced3::GetStatisticsEx
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
-	IWMWriterAdvanced3.GetStatisticsEx
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterAdvanced3::GetStatisticsEx method


## -description



The <b>GetStatisticsEx</b> method retrieves extended statistics for the writer.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which you want to get statistics. You can pass 0 to obtain extended statistics for the entire file. Stream numbers are in the range of 1 through 63.


### -param pStats [out]

Pointer to the <a href="https://msdn.microsoft.com/f98a5934-968e-4c74-9fd2-f824ad77692c">WM_WRITER_STATISTICS_EX</a> structure that receives the statistics.


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
The writer is in the configuration state, during which this method cannot be called.

</td>
</tr>
</table>
 




## -remarks



<b>GetStatisticsEx</b> is not an improved version of <a href="https://msdn.microsoft.com/005c2039-e821-42ab-bead-1bf40f2ab171">IWMWriterAdvanced::GetStatistics</a>. The statistics retrieved by <b>GetStatistics</b> are not retrieved by <b>GetStatisticsEx</b>; if you want to get all available statistics you must call both methods.




## -see-also




<a href="https://msdn.microsoft.com/99f7e4f7-0080-498d-b4f1-960c4955b4db">IWMWriterAdvanced3 Interface</a>
 

 

