---
UID: NF:wmsdkidl.IWMOutputMediaProps.GetConnectionName
title: IWMOutputMediaProps::GetConnectionName
author: windows-sdk-content
description: The GetConnectionName method retrieves the name of the connection to be used for output.
old-location: wmformat\iwmoutputmediaprops_getconnectionname.htm
old-project: wmformat
ms.assetid: 93367398-07aa-4c14-85c8-e3a904bd4564
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetConnectionName, GetConnectionName method [windows Media Format], GetConnectionName method [windows Media Format],IWMOutputMediaProps interface, IWMOutputMediaProps interface [windows Media Format],GetConnectionName method, IWMOutputMediaProps.GetConnectionName, IWMOutputMediaProps::GetConnectionName, IWMOutputMediaPropsGetConnectionName, wmformat.iwmoutputmediaprops_getconnectionname, wmsdkidl/IWMOutputMediaProps::GetConnectionName
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
-	IWMOutputMediaProps.GetConnectionName
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMOutputMediaProps::GetConnectionName


## -description



The <b>GetConnectionName</b> method retrieves the name of the connection to be used for output.




## -parameters




### -param pwszName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name. Pass <b>NULL</b> to retrieve the length of the name.


### -param pcchName [in, out]

On input, a pointer to a variable containing the length of the <i>pwszName</i> array in wide characters. On output, if the method succeeds, it specifies a pointer to the length of the connection name, including the terminating <b>null</b> character.


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
The <i>pwszName</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>pcchName</i> is not large enough for the requested name.

</td>
</tr>
</table>
 




## -remarks



The reader creates a default connection name for each output that is simply a string representation of the output number, for example "1", "2", "3" and so on.

You should make two calls to <b>GetConnectionName</b>. On the first call, pass <b>NULL</b> as <i>pwszName</i>. On return, the value pointed to by <i>pcchName</i> is set to the number of wide characters, including the terminating <b>null</b> character, required to hold the connection name. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszName</i> on the second call.

This connection name is used to match stream numbers to output numbers. All streams in the file are associated with an <b>IWMStreamConfig</b> object whose connection name matches this one (which can be obtained by a call to <b>IWMStreamConfig::GetConnectionName</b>).




## -see-also




<a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps Interface</a>



<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>



<a href="https://msdn.microsoft.com/04d50606-c355-45d4-9cc1-a8ef37113bf7">IWMStreamConfig::GetConnectionName</a>



<a href="https://msdn.microsoft.com/f9f979c4-a15c-4f2a-b63c-7fe776394fdd">Inputs, Streams and Outputs</a>
 

 

