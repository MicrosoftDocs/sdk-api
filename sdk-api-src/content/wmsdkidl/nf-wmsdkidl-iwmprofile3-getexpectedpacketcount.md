---
UID: NF:wmsdkidl.IWMProfile3.GetExpectedPacketCount
title: IWMProfile3::GetExpectedPacketCount
author: windows-sdk-content
description: The GetExpectedPacketCount method calculates the expected packet count for the specified duration. The packet count returned is only an estimate, and it is based upon the settings of the profile at the time this call is made.
old-location: wmformat\iwmprofile3_getexpectedpacketcount.htm
old-project: wmformat
ms.assetid: ddab3735-06a1-4e03-9abc-0fca635ef759
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetExpectedPacketCount, GetExpectedPacketCount method [windows Media Format], GetExpectedPacketCount method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],GetExpectedPacketCount method, IWMProfile3.GetExpectedPacketCount, IWMProfile3::GetExpectedPacketCount, IWMProfile3GetExpectedPacketCount, wmformat.iwmprofile3_getexpectedpacketcount, wmsdkidl/IWMProfile3::GetExpectedPacketCount
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
-	IWMProfile3.GetExpectedPacketCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile3::GetExpectedPacketCount


## -description



The <b>GetExpectedPacketCount</b> method calculates the expected <a href="wmformat_glossary.htm">packet</a> count for the specified duration. The packet count returned is only an estimate, and it is based upon the settings of the profile at the time this call is made.




## -parameters




### -param msDuration [in]

Specifies the duration in milliseconds.


### -param pcPackets [out]

Pointer to receive the count of packets expected for <i>msDuration</i> milliseconds.


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
<i>pcPackets</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
One of the internal objects required by the method could not be initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The profile in the profile object is not compatible with this method.

</td>
</tr>
</table>
 




## -remarks



Problems will arise if the value passed in <i>msDuration</i> is not a positive number of milliseconds. The method will return S_OK as normal, but the packet count returned will not be correct.

It is impossible for this method to give exact counts, because there is no way to account for interleaved data in an encoded file. The packet count returned is most accurate for files with one audio stream. The more complicated the profile, the less accurate the packet count will be.




## -see-also




<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3 Interface</a>
 

 

