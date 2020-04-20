---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetClientInfo
title: IWMReaderAdvanced::SetClientInfo (wmsdkidl.h)
description: The SetClientInfo method sets client-side information used for logging.helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","SetClientInfo method","IWMReaderAdvanced.SetClientInfo","IWMReaderAdvanced::SetClientInfo","IWMReaderAdvancedSetClientInfo","SetClientInfo","SetClientInfo method [windows Media Format]","SetClientInfo method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_setclientinfo","wmsdkidl/IWMReaderAdvanced::SetClientInfo"]
old-location: wmformat\iwmreaderadvanced_setclientinfo.htm
tech.root: wmformat
ms.assetid: dec93690-8285-4672-bf70-63f3c10294bf
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetClientInfo method, IWMReaderAdvanced.SetClientInfo, IWMReaderAdvanced::SetClientInfo, IWMReaderAdvancedSetClientInfo, SetClientInfo, SetClientInfo method [windows Media Format], SetClientInfo method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setclientinfo, wmsdkidl/IWMReaderAdvanced::SetClientInfo
f1_keywords:
- wmsdkidl/IWMReaderAdvanced.SetClientInfo
dev_langs:
- c++
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
- IWMReaderAdvanced.SetClientInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced::SetClientInfo


## -description



The <b>SetClientInfo</b> method sets client-side information used for logging. Use this method to specify information about the client that the reader object sends to the server for logging. If the application does not call this method, the reader object uses default values.




## -parameters




### -param pClientInfo [in]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo">WM_READER_CLIENTINFO</a> structure allocated by the caller, which contains information about the client.


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
Invalid argument. The <b>cbSize</b> member must be set, and the string values must not exceed 1024 characters.

</td>
</tr>
</table>
 




## -remarks



Initialize the <b>WM_READER_CLIENTINFO</b> structure before calling this method. Always set the <b>cbSize</b> member equal to the size of the structure, and set any unused fields to zero.


```cpp

WM_READER_CLIENTINFO info;
ZeroMemory(&info, sizeof(WM_READER_CLIENTINFO));
info.cbSize = sizeof(WM_READER_CLIENTINFO);

// Set other fields (not shown).

hr = pReaderAdvanced->SetClientInfo( &info );

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/client">Client Logging</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>
 

 

