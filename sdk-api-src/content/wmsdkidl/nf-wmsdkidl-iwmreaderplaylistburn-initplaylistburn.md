---
UID: NF:wmsdkidl.IWMReaderPlaylistBurn.InitPlaylistBurn
title: IWMReaderPlaylistBurn::InitPlaylistBurn (wmsdkidl.h)
description: The InitPlaylistBurn method initiates the playlist burning process, by checking the files in the playlist to ensure that they are licensed for copying as part of a playlist.helpviewer_keywords: ["IWMReaderPlaylistBurn interface [windows Media Format]","InitPlaylistBurn method","IWMReaderPlaylistBurn.InitPlaylistBurn","IWMReaderPlaylistBurn::InitPlaylistBurn","IWMReaderPlaylistBurnInitPlaylistBurn","InitPlaylistBurn","InitPlaylistBurn method [windows Media Format]","InitPlaylistBurn method [windows Media Format]","IWMReaderPlaylistBurn interface","wmformat.iwmreaderplaylistburn_initplaylistburn","wmsdkidl/IWMReaderPlaylistBurn::InitPlaylistBurn"]
old-location: wmformat\iwmreaderplaylistburn_initplaylistburn.htm
tech.root: wmformat
ms.assetid: a20a70af-49bc-408f-8c64-779525436f8d
ms.date: 12/05/2018
ms.keywords: IWMReaderPlaylistBurn interface [windows Media Format],InitPlaylistBurn method, IWMReaderPlaylistBurn.InitPlaylistBurn, IWMReaderPlaylistBurn::InitPlaylistBurn, IWMReaderPlaylistBurnInitPlaylistBurn, InitPlaylistBurn, InitPlaylistBurn method [windows Media Format], InitPlaylistBurn method [windows Media Format],IWMReaderPlaylistBurn interface, wmformat.iwmreaderplaylistburn_initplaylistburn, wmsdkidl/IWMReaderPlaylistBurn::InitPlaylistBurn
f1_keywords:
- wmsdkidl/IWMReaderPlaylistBurn.InitPlaylistBurn
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
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
- IWMReaderPlaylistBurn.InitPlaylistBurn
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderPlaylistBurn::InitPlaylistBurn


## -description



The <b>InitPlaylistBurn</b> method initiates the playlist burning process, by checking the files in the playlist to ensure that they are licensed for copying as part of a playlist.




## -parameters




### -param cFiles [in]

Number of files in the playlist. This is also the number of members in the array of file names referenced by <i>pwszFilenames</i>.


### -param ppwszFilenames [in]

Address of an array of <b>WCHAR</b> strings. Each string contains the name of a file in the playlist. You must maintain the file order exactly as it exists in the playlist.


### -param pCallback [in]

Address of the <b>IWMStatusCallback</b> implementation that will receive the WMT_INIT_PLAYLIST_BURN status message.


### -param pvContext [in]

Generic pointer, for use by the application. This is passed to the application in calls to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> callback. You can use this parameter to differentiate between messages from different objects when sharing a single status callback.


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



This method executes asynchronously. When it is finished, a WMT_INIT_PLAYLIST_BURN message is sent to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">OnStatus</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a> interface identified by the <i>pCallback</i> parameter.

The files are checked to determine whether they are DRM-protected. If a file is protected, its license is checked to verify that the license allows copying to CD as part of a playlist.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn">IWMReaderPlaylistBurn Interface</a>
 

 

