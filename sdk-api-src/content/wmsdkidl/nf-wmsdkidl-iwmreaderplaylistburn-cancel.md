---
UID: NF:wmsdkidl.IWMReaderPlaylistBurn.Cancel
title: IWMReaderPlaylistBurn::Cancel
author: windows-sdk-content
description: The Cancel method cancels an initiated playlist burn before initialization is finished.
old-location: wmformat\iwmreaderplaylistburn_cancel.htm
old-project: wmformat
ms.assetid: d126f13b-90ac-489e-8dd0-e507f4003a7a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Cancel, Cancel method [windows Media Format], Cancel method [windows Media Format],IWMReaderPlaylistBurn interface, IWMReaderPlaylistBurn interface [windows Media Format],Cancel method, IWMReaderPlaylistBurn.Cancel, IWMReaderPlaylistBurn::Cancel, IWMReaderPlaylistBurnCancel, wmformat.iwmreaderplaylistburn_cancel, wmsdkidl/IWMReaderPlaylistBurn::Cancel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
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
 - IWMReaderPlaylistBurn.Cancel
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderPlaylistBurn::Cancel


## -description



The <b>Cancel</b> method cancels an initiated playlist burn before initialization is finished.




## -parameters






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



You should call this method to cancel the playlist burn process only after calling <a href="https://msdn.microsoft.com/a20a70af-49bc-408f-8c64-779525436f8d">InitPlaylistBurn</a> and before your status callback receives the WMT_INIT_PLAYLIST_BURN message. If you need to cancel the playlist burn after initialization is finished, you should call the <a href="https://msdn.microsoft.com/355f23eb-3cdb-4c27-bc48-499f349aef2b">EndPlaylistBurn</a> method and pass the E_ABORT error code.




## -see-also




<a href="https://msdn.microsoft.com/a0e1a4f3-4226-44a2-b38e-e5512fda2048">IWMReaderPlaylistBurn Interface</a>
 

 

