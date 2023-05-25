---
UID: NF:wmsdkidl.IWMDRMReader.Individualize
title: IWMDRMReader::Individualize (wmsdkidl.h)
description: The Individualize method individualizes the client by updating their DRM system components.
helpviewer_keywords: ["IWMDRMReader interface [windows Media Format]","Individualize method","IWMDRMReader.Individualize","IWMDRMReader::Individualize","IWMDRMReaderIndividualize","Individualize","Individualize method [windows Media Format]","Individualize method [windows Media Format]","IWMDRMReader interface","wmformat.iwmdrmreader_individualize","wmsdkidl/IWMDRMReader::Individualize"]
old-location: wmformat\iwmdrmreader_individualize.htm
tech.root: wmformat
ms.assetid: 51bf9aa0-4c96-4c0b-8e5e-b63fd20dcc4d
ms.date: 4/26/2023
ms.keywords: IWMDRMReader interface [windows Media Format],Individualize method, IWMDRMReader.Individualize, IWMDRMReader::Individualize, IWMDRMReaderIndividualize, Individualize, Individualize method [windows Media Format], Individualize method [windows Media Format],IWMDRMReader interface, wmformat.iwmdrmreader_individualize, wmsdkidl/IWMDRMReader::Individualize
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
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDRMReader::Individualize
 - wmsdkidl/IWMDRMReader::Individualize
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
 - IWMDRMReader.Individualize
---

# IWMDRMReader::Individualize


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>Individualize</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>Individualize</b> method individualizes the client by updating their DRM system components.

## -parameters

### -param dwFlags [in]

<b>DWORD</b> containing the relevant flags.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0x0</td>
<td>Indicates that the client can be individualized again.</td>
</tr>
<tr>
<td>0x1</td>
<td>Indicates that the client will not be individualized again.</td>
</tr>
</table>

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
A null or invalid argument has been passed in.

</td>
</tr>
</table>

## -remarks

This is an asynchronous call that returns immediately. To abandon the attempt, call <b>CancelIndividualization</b>.

<div class="alert"><b>Important</b>  Because this operation will cause the user's system to be modified, you should display a message that explains what this operation will do and let the user choose whether or not to individualize. For more information and suggested message text, see <a href="/windows/desktop/wmformat/drm-individualization">DRM Individualization</a>.</div>
<div> </div>
Individualization is the process of making the DRM client unique by downloading and installing an individualized component from the Microsoft Individualization Service. The entire process is performed automatically after an application calls the <b>Individualize</b> method. The application is informed of the progress of the individualization process through repeated <b>WMT_INDIVIDUALIZE</b> events, each of which has an associated <a href="/windows/desktop/wmformat/wm-individualize-status">WM_INDIVIDUALIZE_STATUS</a> structure which is sent to the application's <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> callback method.

There are two times to initiate the individualization process: the first is when a piece of content requires it, and the second is when a player individualizes the client as part of the setup. In the latter case, there is no reason to individualize the client again.

## -see-also

<a href="/windows/desktop/wmformat/drm-individualization">DRM Individualization</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization">IWMDRMReader::CancelIndividualization</a>



<a href="/windows/desktop/wmformat/individualizing-drm-applications">Individualizing DRM Applications</a>



<a href="/windows/desktop/wmformat/wm-individualize-status">WM_INDIVIDUALIZE_STATUS</a>