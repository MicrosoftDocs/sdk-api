---
UID: NF:wmsdkidl.IWMReaderTimecode.GetTimecodeRangeCount
title: IWMReaderTimecode::GetTimecodeRangeCount
author: windows-driver-content
description: The GetTimecodeRangeCount method retrieves the total number of SMTPE time code ranges in a specified stream.
old-location: wmformat\iwmreadertimecode_gettimecoderangecount.htm
old-project: wmformat
ms.assetid: df58f968-23f8-407b-b18c-569732635464
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetTimecodeRangeCount, GetTimecodeRangeCount method [windows Media Format], GetTimecodeRangeCount method [windows Media Format],IWMReaderTimecode interface, IWMReaderTimecode interface [windows Media Format],GetTimecodeRangeCount method, IWMReaderTimecode.GetTimecodeRangeCount, IWMReaderTimecode::GetTimecodeRangeCount, IWMReaderTimecodeGetTimecodeRangeCount, wmformat.iwmreadertimecode_gettimecoderangecount, wmsdkidl/IWMReaderTimecode::GetTimecodeRangeCount
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
-	IWMReaderTimecode.GetTimecodeRangeCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderTimecode::GetTimecodeRangeCount


## -description



The <b>GetTimecodeRangeCount</b> method retrieves the total number of SMTPE time code ranges in a specified stream.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. This stream must be indexed by time code.


### -param pwRangeCount [out]

Pointer to a <b>WORD</b> containing the number of ranges. If this parameter is 0 on method return, no SMPTE ranges exist in the stream.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7f7d5608-c505-46ab-9e1e-e45b383c879b">IWMReaderTimecode Interface</a>



<a href="https://msdn.microsoft.com/5bc1f21c-0aca-4e45-ac82-898cb8b9f4cc">IWMReaderTimecode::GetTimecodeRangeBounds</a>
 

 

