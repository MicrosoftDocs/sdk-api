---
UID: NF:wmsdkidl.IWMMutualExclusion2.SetRecordName
title: IWMMutualExclusion2::SetRecordName
author: windows-sdk-content
description: The SetRecordName method assigns a name to a record. You should assign a name to every record so that you can easily identify the records in the future.
old-location: wmformat\iwmmutualexclusion2_setrecordname.htm
old-project: wmformat
ms.assetid: 9527024e-2d52-4a81-90a5-4ef5241ba6dd
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IWMMutualExclusion2 interface [windows Media Format],SetRecordName method, IWMMutualExclusion2.SetRecordName, IWMMutualExclusion2::SetRecordName, IWMMutualExclusion2SetRecordName, SetRecordName, SetRecordName method [windows Media Format], SetRecordName method [windows Media Format],IWMMutualExclusion2 interface, wmformat.iwmmutualexclusion2_setrecordname, wmsdkidl/IWMMutualExclusion2::SetRecordName
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
 - IWMMutualExclusion2.SetRecordName
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMMutualExclusion2::SetRecordName


## -description



The <b>SetRecordName</b> method assigns a name to a record. You should assign a name to every record so that you can easily identify the records in the future.




## -parameters




### -param wRecordNumber [in]

<b>WORD</b> containing the record number to which you want to assign a name.


### -param pwszRecordName [in]

Pointer to a wide-character null-terminated string containing the name you want to assign to the record. Record names are limited to 256 wide characters.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory for the name.

</td>
</tr>
</table>
 




## -remarks



If you pass an empty string as <i>pwszRecordName</i>, the method returns S_OK, but nothing is done.




## -see-also




<a href="https://msdn.microsoft.com/4a1f468c-2ba5-48a1-b56f-8b62aacf1ccf">IWMMutualExclusion2 Interface</a>



<a href="https://msdn.microsoft.com/7508a473-77ae-49ce-b041-2d171193e730">IWMMutualExclusion2::GetRecordName</a>
 

 

