---
UID: NF:wmsdkidl.IWMDRMReader3.GetInclusionList
title: IWMDRMReader3::GetInclusionList (wmsdkidl.h)
description: The GetInclusionList method retrieves a list of identifiers specifying approved protection systems.
helpviewer_keywords: ["GetInclusionList","GetInclusionList method [windows Media Format]","GetInclusionList method [windows Media Format]","IWMDRMReader3 interface","IWMDRMReader3 interface [windows Media Format]","GetInclusionList method","IWMDRMReader3.GetInclusionList","IWMDRMReader3::GetInclusionList","IWMDRMReader3GetInclusionList","wmformat.iwmdrmreader3_getinclusionlist","wmsdkidl/IWMDRMReader3::GetInclusionList"]
old-location: wmformat\iwmdrmreader3_getinclusionlist.htm
tech.root: wmformat
ms.assetid: ac6f2ced-d60d-4472-8549-c52314375ac6
ms.date: 4/26/2023
ms.keywords: GetInclusionList, GetInclusionList method [windows Media Format], GetInclusionList method [windows Media Format],IWMDRMReader3 interface, IWMDRMReader3 interface [windows Media Format],GetInclusionList method, IWMDRMReader3.GetInclusionList, IWMDRMReader3::GetInclusionList, IWMDRMReader3GetInclusionList, wmformat.iwmdrmreader3_getinclusionlist, wmsdkidl/IWMDRMReader3::GetInclusionList
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 11 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDRMReader3::GetInclusionList
 - wmsdkidl/IWMDRMReader3::GetInclusionList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMDRMReader3.GetInclusionList
---

# IWMDRMReader3::GetInclusionList


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>GetInclusionList</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GetInclusionList</b> method retrieves a list of identifiers specifying approved protection systems.

## -parameters

### -param ppGuids [out]

Address of a variable that receives a pointer to an array of identifiers. The array is allocated by using <b>CoTaskMemAlloc</b>. When finished with the list, release the memory by calling <b>CoTaskMemFree</b>.

### -param pcGuids [out]

Number of elements in the array received by the <i>ppGuids</i> parameter.

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

The license issuer can specify other protection systems to which the encrypted content may be converted. The list of GUIDs retrieved by this method identifies the allowed protection systems. When you enter into a license agreement with Microsoft to get the stub library, you will receive a list of currently supported protection systems and the GUIDs used to identify them.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader3">IWMDRMReader3 Interface</a>