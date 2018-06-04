---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# ISBE2Crossbar::EnableDefaultMode


## -description



      Enables or disables the profile default mode and stream default mode for a crossbar in a <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter.
    The <i>profile</i>  describes a set of media types that can be used to create out pins, one media type per output pin. The <i>stream mapping</i> describes the mappings between the streams within a WTV file and filter output pins.

 If you do not call the <b>EnableDefaultMode</b> method in your application, the crossbar uses a default profile and a default stream map. In this case, the crossbar is said to be in <i>profile default mode</i> and <i>stream default mode</i>, respectively. You can use the <b>EnableDefaultMode</b> method to disable either mode or both modes, so that you can specify custom profiles or stream mappings. You can also use an <code>EnableDefaultMode(FALSE)</code> call to disable both default modes.


## -parameters




### -param DefaultFlags [in]

Specifies the default modes for the crossbar. This can be any combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>DEF_MODE_PROFILE</dt>
</dl>
</td>
<td width="60%">
Enables profile default mode. The default profile is used, and you cannot specify custom profiles by calling the <a href="https://msdn.microsoft.com/34067ca5-ead0-44ac-b274-dc9e3f2fb2fd">SetOutputProfile</a> method. If you omit this flag, profile default mode is disabled  so that you can specify a custom output profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>DEF_MODE_STREAMS</dt>
</dl>
</td>
<td width="60%">
Enables stream default mode. The Stream Buffer Enging (SBE) handles the mapping between streams and output pins, and you cannot change these mappings by calling the <a href="https://msdn.microsoft.com/efe3b21d-9664-4367-9bfe-4c02589370c4">ISBE2StreamMap::MapStream</a> method. If you omit this flag, stream default mode is disabled,  so that you can specify a custom mapping.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In stream default mode, SBE first checks the Windows Media Center TV settings to determine if a preferred language is set. If a preferred language is set:

<ul>
<li>If an audio stream in the preferred language exists, SBE outputs that audio stream.</li>
<li>If an audio stream in the preferred language does not exist, SBE outputs the default audio stream, which is set when the stream is captured.</li>
</ul>
If no preferred language is set, Windows Media Center is either not present or not configured. In this case:

<ul>
<li>If an audio stream in the language the operating system locale exists, SBE outputs that audio stream.</li>
<li>Otherwise, SBE outputs the default audio stream.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/299816e7-2dad-44a5-a44d-9c3efe405d9b">ISBE2Crossbar</a>



<a href="https://msdn.microsoft.com/34067ca5-ead0-44ac-b274-dc9e3f2fb2fd">ISBE2Crossbar::SetOutputProfile</a>



<a href="https://msdn.microsoft.com/efe3b21d-9664-4367-9bfe-4c02589370c4">ISBE2StreamMap::MapStream</a>



<a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source Filter</a>
 

 

