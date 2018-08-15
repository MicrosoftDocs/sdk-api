---
UID: NF:wmsdkidl.IWMWriterAdvanced.GetSyncTolerance
title: IWMWriterAdvanced::GetSyncTolerance
author: windows-sdk-content
description: The GetSyncTolerance method retrieves the amount of time during which the inputs can fall out of synchronization before the samples are discarded.
old-location: wmformat\iwmwriteradvanced_getsynctolerance.htm
old-project: wmformat
ms.assetid: f62d3405-3125-4df6-bd06-fa70358560ad
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetSyncTolerance, GetSyncTolerance method [windows Media Format], GetSyncTolerance method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],GetSyncTolerance method, IWMWriterAdvanced.GetSyncTolerance, IWMWriterAdvanced::GetSyncTolerance, IWMWriterAdvancedGetSyncTolerance, wmformat.iwmwriteradvanced_getsynctolerance, wmsdkidl/IWMWriterAdvanced::GetSyncTolerance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMWriterAdvanced.GetSyncTolerance
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterAdvanced::GetSyncTolerance


## -description



The <b>GetSyncTolerance</b> method retrieves the amount of time during which the inputs can fall out of synchronization before the samples are discarded.




## -parameters




### -param pmsWindow [in]

Pointer to the limit of the number of milliseconds that the inputs can be out of synchronization. Note that this parameter is in milliseconds and not 100-nanosecond units.


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
<i>pmsWindow</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The default tolerance is 3000 milliseconds.




## -see-also




<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/d60020bf-52f1-46a0-aeae-367e3b179fac">IWMWriterAdvanced::SetSyncTolerance</a>
 

 

