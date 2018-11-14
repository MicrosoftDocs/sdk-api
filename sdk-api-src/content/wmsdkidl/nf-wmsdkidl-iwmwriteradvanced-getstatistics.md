---
UID: NF:wmsdkidl.IWMWriterAdvanced.GetStatistics
title: IWMWriterAdvanced::GetStatistics
author: windows-sdk-content
description: The GetStatistics method retrieves statistics describing the current writing operation.
old-location: wmformat\iwmwriteradvanced_getstatistics.htm
tech.root: wmformat
ms.assetid: 005c2039-e821-42ab-bead-1bf40f2ab171
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetStatistics, GetStatistics method [windows Media Format], GetStatistics method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],GetStatistics method, IWMWriterAdvanced.GetStatistics, IWMWriterAdvanced::GetStatistics, IWMWriterAdvancedGetStatistics, wmformat.iwmwriteradvanced_getstatistics, wmsdkidl/IWMWriterAdvanced::GetStatistics
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
 - IWMWriterAdvanced.GetStatistics
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
- IWMWriterAdvanced.GetStatistics
: 
---

# IWMWriterAdvanced::GetStatistics


## -description



The <b>GetStatistics</b> method retrieves statistics describing the current writing operation.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers must be in the range of 1 through 63. A value of 0 retrieves statistics for the file as a whole.


### -param pStats [out]

Pointer to a <a href="https://msdn.microsoft.com/907711c9-2ae1-4049-afd8-768912778e37">WM_WRITER_STATISTICS</a> structure that receives the statistics.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pStats</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/3ea41491-409c-42b7-a4b2-f0d7c222c299">IWMWriterAdvanced3::GetStatisticsEx</a>
 

 

