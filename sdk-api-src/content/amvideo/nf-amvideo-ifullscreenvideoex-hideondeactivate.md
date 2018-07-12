---
UID: NF:amvideo.IFullScreenVideoEx.HideOnDeactivate
title: IFullScreenVideoEx::HideOnDeactivate
author: windows-sdk-content
description: The HideOnDeactivate method . Depending on the setting, the full-screen video window is either minimized or hidden. If it is minimized, it appears as an icon in the task bar; otherwise, it does not.
old-location: dshow\ifullscreenvideoex_hideondeactivate.htm
old-project: DirectShow
ms.assetid: b2839876-40b1-4b41-a3a4-99e5cbdd9ef1
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: HideOnDeactivate, HideOnDeactivate method [DirectShow], HideOnDeactivate method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],HideOnDeactivate method, IFullScreenVideoEx.HideOnDeactivate, IFullScreenVideoEx::HideOnDeactivate, IFullScreenVideoHideOnDeactivate, amvideo/IFullScreenVideoEx::HideOnDeactivate, dshow.ifullscreenvideoex_hideondeactivate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx.HideOnDeactivate
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IFullScreenVideoEx::HideOnDeactivate


## -description



The <code>HideOnDeactivate</code> method . Depending on the setting, the full-screen video window is either minimized or hidden. If it is minimized, it appears as an icon in the task bar; otherwise, it does not.




## -parameters




### -param Hide [in]

Value that specifies the behavior when the application is deactivated. Set to OATRUE to hide the icon; set to OAFALSE to display the icon.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Hide the video window.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Minimize the video window. (Default)</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

