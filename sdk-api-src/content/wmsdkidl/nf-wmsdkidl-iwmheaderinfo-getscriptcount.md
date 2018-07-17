---
UID: NF:wmsdkidl.IWMHeaderInfo.GetScriptCount
title: IWMHeaderInfo::GetScriptCount
author: windows-sdk-content
description: The GetScriptCount method returns the number of scripts currently in the header section of the ASF file.
old-location: wmformat\iwmheaderinfo_getscriptcount.htm
old-project: wmformat
ms.assetid: c1a0b35c-db05-402a-9bde-684bead1eedf
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetScriptCount, GetScriptCount method [windows Media Format], GetScriptCount method [windows Media Format],IWMHeaderInfo interface, GetScriptCount method [windows Media Format],IWMHeaderInfo2 interface, GetScriptCount method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetScriptCount method, IWMHeaderInfo.GetScriptCount, IWMHeaderInfo2 interface [windows Media Format],GetScriptCount method, IWMHeaderInfo2::GetScriptCount, IWMHeaderInfo3 interface [windows Media Format],GetScriptCount method, IWMHeaderInfo3::GetScriptCount, IWMHeaderInfo::GetScriptCount, IWMHeaderInfoGetScriptCount, wmformat.iwmheaderinfo_getscriptcount, wmsdkidl/IWMHeaderInfo2::GetScriptCount, wmsdkidl/IWMHeaderInfo3::GetScriptCount, wmsdkidl/IWMHeaderInfo::GetScriptCount
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
 - IWMHeaderInfo.GetScriptCount
 - IWMHeaderInfo2.GetScriptCount
 - IWMHeaderInfo3.GetScriptCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMHeaderInfo::GetScriptCount


## -description



The <b>GetScriptCount</b> method returns the number of scripts currently in the header section of the ASF file.




## -parameters




### -param pcScripts [out]

Pointer to a count of scripts.


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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a configurable state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pcScripts</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pcScripts</i> is not a valid pointer.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2</a>



<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a>



<a href="https://msdn.microsoft.com/779a7618-9f22-4caf-8a4e-b622e422c30d">IWMHeaderInfo::GetScript</a>
 

 

