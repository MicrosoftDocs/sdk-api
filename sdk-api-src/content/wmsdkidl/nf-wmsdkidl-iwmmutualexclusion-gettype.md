---
UID: NF:wmsdkidl.IWMMutualExclusion.GetType
title: IWMMutualExclusion::GetType
author: windows-sdk-content
description: The GetType method retrieves the GUID of the type of mutual exclusion required.
old-location: wmformat\iwmmutualexclusion_gettype.htm
old-project: wmformat
ms.assetid: 546bb0d1-a11e-4bf7-92fc-cef938d792bb
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetType, GetType method [windows Media Format], GetType method [windows Media Format],IWMMutualExclusion interface, IWMMutualExclusion interface [windows Media Format],GetType method, IWMMutualExclusion.GetType, IWMMutualExclusion::GetType, IWMMutualExclusionGetType, wmformat.iwmmutualexclusion_gettype, wmsdkidl/IWMMutualExclusion::GetType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IWMMutualExclusion.GetType
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMMutualExclusion::GetType


## -description



The <b>GetType</b> method retrieves the GUID of the type of mutual exclusion required.




## -parameters




### -param pguidType [out]

Pointer to a GUID that specifies the type of mutual exclusion.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pguidType</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The following constants represent the GUIDs supported by this SDK.

<table>
<tr>
<th>
              Mutual exclusion type identifier
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>CLSID_WMMUTEX_Bitrate</td>
<td>The mutual exclusion streams differ only in bit rate. On playback, the stream that will best use the available bandwidth is chosen. You must use this type of mutual exclusion for multiple bit rate files.</td>
</tr>
<tr>
<td>CLSID_WMMUTEX_Language</td>
<td>The mutual exclusion streams are the same content only in a different language. A common use of this type of mutual exclusion is for dubbing soundtracks into multiple languages.</td>
</tr>
<tr>
<td>CLSID_WMMUTEX_Presentation</td>
<td>The mutual exclusion streams are the same video in a different presentation format. The presentation format is usually defined by the aspect ratio of the video frame.</td>
</tr>
<tr>
<td>CLSID_WMMUTEX_Unknown</td>
<td>The mutual exclusion streams are of a custom type. This sort of mutual exclusion can contain streams of varying types.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If you create a multiple bit rate audio file, you may encounter problems streaming the file from Windows Media Services 4.1. To avoid problems, disable auto indexing with a call to <a href="https://msdn.microsoft.com/6c8f1c25-d752-42b6-87b7-9d6a6e38642f">IWMWriterFileSink3::SetAutoIndexing</a> before writing the file.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/040635fb-de00-4c8c-9c39-c28c409311c3">IWMMutualExclusion Interface</a>



<a href="https://msdn.microsoft.com/18796219-bc33-41b7-b2af-a23585c2500a">IWMMutualExclusion::SetType</a>
 

 

