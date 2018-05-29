---
UID: NF:wmsdkidl.IWMMutualExclusion2.GetRecordName
title: IWMMutualExclusion2::GetRecordName
author: windows-sdk-content
description: The GetRecordName method retrieves the name of the specified record. A record has a name only if a name has been assigned using the IWMMutualExclusion2::SetRecordName method.
old-location: wmformat\iwmmutualexclusion2_getrecordname.htm
old-project: wmformat
ms.assetid: 7508a473-77ae-49ce-b041-2d171193e730
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetRecordName, GetRecordName method [windows Media Format], GetRecordName method [windows Media Format],IWMMutualExclusion2 interface, IWMMutualExclusion2 interface [windows Media Format],GetRecordName method, IWMMutualExclusion2.GetRecordName, IWMMutualExclusion2::GetRecordName, IWMMutualExclusion2GetRecordName, wmformat.iwmmutualexclusion2_getrecordname, wmsdkidl/IWMMutualExclusion2::GetRecordName
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
-	IWMMutualExclusion2.GetRecordName
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMMutualExclusion2::GetRecordName


## -description



The <b>GetRecordName</b> method retrieves the name of the specified record. A record has a name only if a name has been assigned using the <a href="https://msdn.microsoft.com/9527024e-2d52-4a81-90a5-4ef5241ba6dd">IWMMutualExclusion2::SetRecordName</a> method.




## -parameters




### -param wRecordNumber [in]

<b>WORD</b> containing the number of the record for which you want to get the name.


### -param pwszRecordName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the record name. Pass <b>NULL</b> to retrieve the length of the name.


### -param pcchRecordName [in, out]

On input, a pointer to a variable containing the length of the <i>pwszRecordName</i> array in wide characters (2 bytes). On output, if the method succeeds, the variable contains the length of the name, including the terminating <b>null</b> character. However, if you pass <b>NULL</b> as <i>pwszRecordName</i>, this will be set to the required length on output.


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
<i>wRecordNumber</i> does not contain a valid record number.

OR

<i>pcchRecordName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to access the record for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetRecordName</b> for each record name you want to retrieve. On the first call, pass <b>NULL</b> as <i>pwszRecordName</i>. On return, the value pointed to by <i>pcchRecordName</i> will be set to the number of wide characters, including the terminating <b>null</b> character, required to hold the record name. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszRecordName</i> on the second call.

Records are assigned numbers sequentially in the order they are created.




## -see-also




<a href="https://msdn.microsoft.com/4a1f468c-2ba5-48a1-b56f-8b62aacf1ccf">IWMMutualExclusion2 Interface</a>
 

 

