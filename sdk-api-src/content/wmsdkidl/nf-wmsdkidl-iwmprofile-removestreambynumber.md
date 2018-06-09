---
UID: NF:wmsdkidl.IWMProfile.RemoveStreamByNumber
title: IWMProfile::RemoveStreamByNumber
author: windows-sdk-content
description: The RemoveStreamByNumber method removes a stream from the profile.
old-location: wmformat\iwmprofile_removestreambynumber.htm
old-project: wmformat
ms.assetid: 72ecc794-d393-416e-bc21-5a7756e76d99
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMProfile interface [windows Media Format],RemoveStreamByNumber method, IWMProfile.RemoveStreamByNumber, IWMProfile2 interface [windows Media Format],RemoveStreamByNumber method, IWMProfile2::RemoveStreamByNumber, IWMProfile3 interface [windows Media Format],RemoveStreamByNumber method, IWMProfile3::RemoveStreamByNumber, IWMProfile::RemoveStreamByNumber, IWMProfileRemoveStreamByNumber, RemoveStreamByNumber, RemoveStreamByNumber method [windows Media Format], RemoveStreamByNumber method [windows Media Format],IWMProfile interface, RemoveStreamByNumber method [windows Media Format],IWMProfile2 interface, RemoveStreamByNumber method [windows Media Format],IWMProfile3 interface, wmformat.iwmprofile_removestreambynumber, wmsdkidl/IWMProfile2::RemoveStreamByNumber, wmsdkidl/IWMProfile3::RemoveStreamByNumber, wmsdkidl/IWMProfile::RemoveStreamByNumber
ms.prod: windows
ms.technology: windows-sdk
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
 - qasf.dll
api_name:
 - IWMProfile.RemoveStreamByNumber
 - IWMProfile2.RemoveStreamByNumber
 - IWMProfile3.RemoveStreamByNumber
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProfile::RemoveStreamByNumber


## -description



The <b>RemoveStreamByNumber</b> method removes a stream from the profile.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NO_STREAM</b></dt>
</dl>
</td>
<td width="60%">
No stream was found to match <i>wStreamNum</i> value.

</td>
</tr>
</table>
 




## -remarks



A stream may be included in other objects within the profile, such as mutual exclusion objects. This method will remove all references to the specified stream from all objects within the profile.

Stream numbers are in the range of 1 through 63.




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>



<a href="https://msdn.microsoft.com/507b1c55-1ecb-41dd-a6e5-298e1047a7ea">IWMProfile::GetStreamByNumber</a>



<a href="https://msdn.microsoft.com/82817b72-fde5-492e-b197-87bf145d0be9">IWMProfile::RemoveStream</a>
 

 

