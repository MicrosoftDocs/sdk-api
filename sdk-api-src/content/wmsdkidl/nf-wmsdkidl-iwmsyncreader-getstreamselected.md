---
UID: NF:wmsdkidl.IWMSyncReader.GetStreamSelected
title: IWMSyncReader::GetStreamSelected
author: windows-driver-content
description: The GetStreamSelected method retrieves a flag indicating whether a particular stream is currently selected.
old-location: wmformat\iwmsyncreader_getstreamselected.htm
old-project: wmformat
ms.assetid: bcde749e-c0fd-4be8-8708-a053854a9275
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetStreamSelected, GetStreamSelected method [windows Media Format], GetStreamSelected method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetStreamSelected method, IWMSyncReader.GetStreamSelected, IWMSyncReader::GetStreamSelected, IWMSyncReaderGetStreamSelected, wmformat.iwmsyncreader_getstreamselected, wmsdkidl/IWMSyncReader::GetStreamSelected
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
-	IWMSyncReader.GetStreamSelected
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::GetStreamSelected


## -description



The <b>GetStreamSelected</b> method retrieves a flag indicating whether a particular stream is currently selected.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param pSelection [out]

Pointer to a variable that receives one member of the <a href="https://msdn.microsoft.com/7191d608-1a25-48c0-858b-c5e93f9d8e6e">WMT_STREAM_SELECTION</a> enumeration type on output. This value specifies the selection status for the specified stream.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSelection</i> parameter is <b>NULL</b>, or the stream number is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
No file is open in the synchronous reader.

</td>
</tr>
</table>
 




## -remarks



This method is identical to <a href="https://msdn.microsoft.com/083fc743-79be-43c6-ac4b-458c74f42fa0">IWMReaderAdvanced::GetStreamSelected</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>
 

 

