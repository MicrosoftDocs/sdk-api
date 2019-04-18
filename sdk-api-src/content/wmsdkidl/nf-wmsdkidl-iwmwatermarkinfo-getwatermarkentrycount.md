---
UID: NF:wmsdkidl.IWMWatermarkInfo.GetWatermarkEntryCount
title: IWMWatermarkInfo::GetWatermarkEntryCount (wmsdkidl.h)
author: windows-sdk-content
description: The GetWatermarkEntryCount method retrieves the total number of installed watermarking systems of a specified type. Use this method in conjunction with IWMWatermarkInfo::GetWatermarkEntry to enumerate the installed watermarking DMOs.
old-location: wmformat\iwmwatermarkinfo_getwatermarkentrycount.htm
tech.root: wmformat
ms.assetid: 27a102b7-a495-49ee-9d65-a0276ca2cf76
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetWatermarkEntryCount, GetWatermarkEntryCount method [windows Media Format], GetWatermarkEntryCount method [windows Media Format],IWMWatermarkInfo interface, IWMWatermarkInfo interface [windows Media Format],GetWatermarkEntryCount method, IWMWatermarkInfo.GetWatermarkEntryCount, IWMWatermarkInfo::GetWatermarkEntryCount, IWMWatermarkInfoGetWatermarkEntryCount, wmformat.iwmwatermarkinfo_getwatermarkentrycount, wmsdkidl/IWMWatermarkInfo::GetWatermarkEntryCount
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
 - IWMWatermarkInfo.GetWatermarkEntryCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWatermarkInfo::GetWatermarkEntryCount


## -description



The <b>GetWatermarkEntryCount</b> method retrieves the total number of installed watermarking systems of a specified type. Use this method in conjunction with <a href="https://msdn.microsoft.com/en-us/library/Dd798717(v=VS.85).aspx">IWMWatermarkInfo::GetWatermarkEntry</a> to enumerate the installed watermarking <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">DMOs</a>.




## -parameters




### -param wmetType [in]

A value from the <a href="https://msdn.microsoft.com/en-us/library/Dd757881(v=VS.85).aspx">WMT_WATERMARK_ENTRY_TYPE</a> enumeration type specifying the type of watermarking system..


### -param pdwCount [out]

Pointer to a <b>DWORD</b> containing the number of watermark entries.


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
 




## -remarks



No watermarking DMOs are provided with the Windows Media Format SDK. You can install third-party DMOs to use with your application.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798716(v=VS.85).aspx">IWMWatermarkInfo Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798717(v=VS.85).aspx">IWMWatermarkInfo::GetWatermarkEntry</a>
 

 

