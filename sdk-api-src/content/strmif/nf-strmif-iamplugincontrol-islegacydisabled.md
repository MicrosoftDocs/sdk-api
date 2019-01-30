---
UID: NF:strmif.IAMPluginControl.IsLegacyDisabled
title: IAMPluginControl::IsLegacyDisabled
author: windows-sdk-content
description: Queries whether an Audio Compression Manager (ACM) or Video Compression Manager (VCM) codec appears in the blocked list.
old-location: dshow\iamplugincontrol_islegacydisabled.htm
tech.root: DirectShow
ms.assetid: f67c7a78-1e4f-469a-9cbb-80c37bba80b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMPluginControl interface [DirectShow],IsLegacyDisabled method, IAMPluginControl.IsLegacyDisabled, IAMPluginControl::IsLegacyDisabled, IsLegacyDisabled, IsLegacyDisabled method [DirectShow], IsLegacyDisabled method [DirectShow],IAMPluginControl interface, dshow.iamplugincontrol_islegacydisabled, strmif/IAMPluginControl::IsLegacyDisabled
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMPluginControl.IsLegacyDisabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMPluginControl::IsLegacyDisabled


## -description


Queries whether an Audio Compression Manager (ACM) or Video Compression Manager (VCM) codec appears in the blocked list.


## -parameters




### -param dllName [in]

The name of the DLL that implements the codec.


## -returns



This method can return one of these values.

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
The specified DLL appears in the blocked list.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The specified DLL is not in the blocked list.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/66720991-3a3f-4c45-a543-b8050d31fcc3">IAMPluginControl</a>



<a href="https://msdn.microsoft.com/938ba1b0-822e-4871-8786-b7eeee243867">Intelligent Connect</a>
 

 

