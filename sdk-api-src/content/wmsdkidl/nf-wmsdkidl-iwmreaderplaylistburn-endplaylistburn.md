---
UID: NF:wmsdkidl.IWMReaderPlaylistBurn.EndPlaylistBurn
title: IWMReaderPlaylistBurn::EndPlaylistBurn
author: windows-sdk-content
description: The EndPlaylistBurn method completes the playlist burn process. This includes releasing resources and adjusting counts associated with rights in DRM licenses.
old-location: wmformat\iwmreaderplaylistburn_endplaylistburn.htm
old-project: wmformat
ms.assetid: 355f23eb-3cdb-4c27-bc48-499f349aef2b
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: EndPlaylistBurn, EndPlaylistBurn method [windows Media Format], EndPlaylistBurn method [windows Media Format],IWMReaderPlaylistBurn interface, IWMReaderPlaylistBurn interface [windows Media Format],EndPlaylistBurn method, IWMReaderPlaylistBurn.EndPlaylistBurn, IWMReaderPlaylistBurn::EndPlaylistBurn, IWMReaderPlaylistBurnEndPlaylistBurn, wmformat.iwmreaderplaylistburn_endplaylistburn, wmsdkidl/IWMReaderPlaylistBurn::EndPlaylistBurn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IWMReaderPlaylistBurn.EndPlaylistBurn
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderPlaylistBurn::EndPlaylistBurn


## -description



The <b>EndPlaylistBurn</b> method completes the playlist burn process. This includes releasing resources and adjusting counts associated with rights in DRM licenses.




## -parameters




### -param hrBurnResult [in]

Result of the playlist burn. Set to S_OK if the files in the playlist were successfully copied to CD. Otherwise, set to an appropriate <b>HRESULT</b> error code.


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



To abort the playlist burn process after your status callback receives the WMT_INIT_PLAYLIST_BURN message, pass the E_ABORT error code. To stop the process before initialization is complete, call the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a> method.




## -see-also




<a href="https://msdn.microsoft.com/a0e1a4f3-4226-44a2-b38e-e5512fda2048">IWMReaderPlaylistBurn Interface</a>
 

 

