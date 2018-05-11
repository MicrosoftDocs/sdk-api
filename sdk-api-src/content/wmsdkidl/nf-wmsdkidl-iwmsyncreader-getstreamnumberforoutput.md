---
UID: NF:wmsdkidl.IWMSyncReader.GetStreamNumberForOutput
title: IWMSyncReader::GetStreamNumberForOutput
author: windows-driver-content
description: The GetStreamNumberForOutput method retrieves the stream number that corresponds with the specified output.
old-location: wmformat\iwmsyncreader_getstreamnumberforoutput.htm
old-project: wmformat
ms.assetid: 85543b80-78dd-4dc6-8885-c6a53f910165
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetStreamNumberForOutput, GetStreamNumberForOutput method [windows Media Format], GetStreamNumberForOutput method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetStreamNumberForOutput method, IWMSyncReader.GetStreamNumberForOutput, IWMSyncReader::GetStreamNumberForOutput, IWMSyncReaderGetStreamNumberForOutput, wmformat.iwmsyncreader_getstreamnumberforoutput, wmsdkidl/IWMSyncReader::GetStreamNumberForOutput
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
-	IWMSyncReader.GetStreamNumberForOutput
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::GetStreamNumberForOutput


## -description



The <b>GetStreamNumberForOutput</b> method retrieves the stream number that corresponds with the specified output.




## -parameters




### -param dwOutputNum




### -param pwStreamNum [out]

Pointer to a <b>WORD</b> value that receives the stream number that corresponds to the output specified by <i>dwOutput</i>.


#### - dwOutput [in]

<b>DWORD</b> value specifying the output number for which you want to retrieve a stream number.


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
<i>dwOutput</i> specifies an invalid output number.

</td>
</tr>
</table>
 




## -remarks



In the case of outputs that equate to mutual exclusions, only the active stream number is retrieved. If you need to get all of the stream numbers associated with such an output, you must access the profile information for the file.




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>
 

 

