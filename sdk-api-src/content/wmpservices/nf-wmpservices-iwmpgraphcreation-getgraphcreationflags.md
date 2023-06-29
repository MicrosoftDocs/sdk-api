---
UID: NF:wmpservices.IWMPGraphCreation.GetGraphCreationFlags
title: IWMPGraphCreation::GetGraphCreationFlags (wmpservices.h)
description: One of the flags documented on this page is available in Windows Media Player 10 and Windows Media Player 11 running on Microsoft Windows XP. It might not be available in subsequent versions.
helpviewer_keywords: ["GetGraphCreationFlags","GetGraphCreationFlags method [Windows Media Player]","GetGraphCreationFlags method [Windows Media Player]","IWMPGraphCreation interface","IWMPGraphCreation interface [Windows Media Player]","GetGraphCreationFlags method","IWMPGraphCreation.GetGraphCreationFlags","IWMPGraphCreation::GetGraphCreationFlags","IWMPGraphCreationGetGraphCreationFlags","wmp.iwmpgraphcreation_getgraphcreationflags","wmpservices/IWMPGraphCreation::GetGraphCreationFlags"]
old-location: wmp\iwmpgraphcreation_getgraphcreationflags.htm
tech.root: WMP
ms.assetid: 26cac321-f32a-4569-87a8-f397173f058b
ms.date: 4/26/2023
ms.keywords: GetGraphCreationFlags, GetGraphCreationFlags method [Windows Media Player], GetGraphCreationFlags method [Windows Media Player],IWMPGraphCreation interface, IWMPGraphCreation interface [Windows Media Player],GetGraphCreationFlags method, IWMPGraphCreation.GetGraphCreationFlags, IWMPGraphCreation::GetGraphCreationFlags, IWMPGraphCreationGetGraphCreationFlags, wmp.iwmpgraphcreation_getgraphcreationflags, wmpservices/IWMPGraphCreation::GetGraphCreationFlags
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPGraphCreation::GetGraphCreationFlags
 - wmpservices/IWMPGraphCreation::GetGraphCreationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPGraphCreation.GetGraphCreationFlags
---

# IWMPGraphCreation::GetGraphCreationFlags


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

One of the flags documented on this page is available in Windows Media Player 10 and Windows Media Player 11 running on Microsoft Windows XP. It might not be available in subsequent versions.
        



The <b>GetGraphCreationFlags</b> method is called by Windows Media Player to retrieve a value that represents the graph creation preferences.

## -parameters

### -param pdwFlags [out]

Address of a <b>DWORD</b> variable that receives a value that represents one or more graph creation flags combined by using bitwise OR operations.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>

## -remarks

The following table describes the graph creation flags.

<table>
<tr>
<th>Flag</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>WMPGC_FLAGS_ALLOW_PREROLL</td>
<td>0x1</td>
<td>Windows Media Player will build the filter graph for the next media item before the current media item finishes playing.</td>
</tr>
<tr>
<td>WMPGC_FLAGS_SUPPRESS_DIALOGS</td>
<td>0x2</td>
<td>Windows Media Player will not display warning dialog boxes when errors occur.</td>
</tr>
<tr>
<td>WMPGC_FLAGS_IGNORE_AV_SYNC</td>
<td>0x4</td>
<td>Windows Media Player will not require audio and video to be synchronized when playing Windows Media-based content (.asf, .wma, or .wmv). Windows Media Player will attempt to play every frame of video. This occurs even when video data is arriving more slowly than audio data. 
					<div class="alert"><b>Note</b>  This flag is supported only in Windows Media Player 10 or 11 running on Microsoft Windows XP.</div>
<div> </div>
</td>
</tr>
<tr>
<td>WMPGC_FLAGS_DISABLE_PLUGINS</td>
<td>0x8</td>
<td>Disables all plug-ins for the current instance of the Windows Media Player control. This includes plug-ins native to Windows Media Player. For example, visualizations will not work when this flag is set.</td>
</tr>
<tr>
<td>WMPGC_FLAGS_USE_CUSTOM_GRAPH</td>
<td>0x10</td>
<td>Windows Media Player will use the application-provided DirectShow graph as-is and not attempt to further render the originally requested URL or file. Plug-ins will still be added to the custom graph unless the <b>WMPGC_FLAGS_DISABLE_PLUGINS</b> flag is also set. Set both these flags if you want WMP to use the provided graph without any changes. Requires Windows Media Player 12.</td>
</tr>
</table>
 

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation">IWMPGraphCreation Interface</a>