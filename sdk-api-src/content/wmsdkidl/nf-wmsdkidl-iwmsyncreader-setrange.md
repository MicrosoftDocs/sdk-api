---
UID: NF:wmsdkidl.IWMSyncReader.SetRange
title: IWMSyncReader::SetRange method
author: windows-driver-content
description: The SetRange method enables you to specify a start time and duration for playback by the synchronous reader.
old-location: wmformat\iwmsyncreader_setrange.htm
old-project: wmformat
ms.assetid: d96c97ad-085d-4753-8efb-8a6bcb284e78
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMSyncReader, IWMSyncReader interface [windows Media Format], SetRange method, IWMSyncReader::SetRange, IWMSyncReaderSetRange, SetRange method [windows Media Format], SetRange method [windows Media Format], IWMSyncReader interface, SetRange,IWMSyncReader.SetRange, wmformat.iwmsyncreader_setrange, wmsdkidl/IWMSyncReader::SetRange
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
-	IWMSyncReader.SetRange
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::SetRange method


## -description



The <b>SetRange</b> method enables you to specify a start time and duration for playback by the synchronous reader.




## -parameters




### -param cnsStartTime [in]

Offset into the file at which to start playback. This value is measured in 100-nanosecond units.


### -param cnsDuration [in]

Duration in 100-nanosecond units, or zero to continue playback to the end of the file.


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
The <i>cnsDuration</i> parameter is negative.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for an internal object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No file is loaded in the synchronous reader.

</td>
</tr>
</table>
 




## -remarks



This method specifies a range for the whole file only. You cannot specify a range for an individual stream.

You can call <b>SetRange</b> at any time after a file has been loaded.

The start time you specify might not be the presentation time of the first sample received. The synchronous delivers video samples starting with the key frame before the specified time.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>



<a href="https://msdn.microsoft.com/3d53838c-0d07-4aa6-8797-9ed7e07cb8fe">IWMSyncReader::SetRangeByFrame</a>
 

 

