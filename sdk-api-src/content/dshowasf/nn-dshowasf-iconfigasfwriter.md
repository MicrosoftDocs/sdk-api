---
UID: NN:dshowasf.IConfigAsfWriter
title: IConfigAsfWriter
author: windows-sdk-content
description: The IConfigAsfWriter interface configures the WM ASF Writer filter.
old-location: dshow\iconfigasfwriter.htm
tech.root: DirectShow
ms.assetid: 50fd7825-4844-4a7f-b949-4abfff5ef30f
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IConfigAsfWriter, IConfigAsfWriter interface [DirectShow], IConfigAsfWriter interface [DirectShow],described, IConfigAsfWriterInterface, dshow.iconfigasfwriter, dshowasf/IConfigAsfWriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAsfWriter interface


## -description



The <code>IConfigAsfWriter</code> interface configures the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> filter. It provides methods for getting and setting the profiles and indexing mode.

When the WM ASF Writer filter is created, it is configured automatically with a default ASF audio-visual profile based on the incoming streams. A profile describes various attributes of an ASF file such as bit rate, number and type of streams, compression quality, and so on. The filter uses the profile to determine what kind of ASF file to write, how many input pins to create, and what media types to accept. When the WM ASF Writer filter is first created, it is configured automatically with the following default profile: WMProfile_V80_256Video. However, using this profile is not recommended because it does not use the Windows Media Audio and Video 9 Series codecs.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConfigAsfWriter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConfigAsfWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConfigAsfWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89156f64-7a20-4226-9f01-5b1bd4a1fe98">ConfigureFilterUsingProfile</a>
</td>
<td align="left" width="63%">
Sets an ASF profile on the WM ASF Writer filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8cfb3b22-aa6b-42e0-bbb5-876932e8bd82">ConfigureFilterUsingProfileGuid</a>
</td>
<td align="left" width="63%">
Sets a predefined system profile on the filter. (Deprecated.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e532001a-e2ff-4ad4-8fef-2fa5b051d1f5">ConfigureFilterUsingProfileId</a>
</td>
<td align="left" width="63%">
Sets a Windows Media Format 4.0 profile on the filter. (Deprecated.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fa9fc3f-f8fd-42c9-9de2-22717cbb7e91">GetCurrentProfile</a>
</td>
<td align="left" width="63%">
Retrieves the application-defined ASF profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8958f8d3-40ff-44b1-a817-5dca30636306">GetCurrentProfileGuid</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the filter's current system profile, if any. (Deprecated.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37288625-368f-41d4-bfdc-bb2fd144f455">GetCurrentProfileId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the filter's profile, only when the filter is using a Windows Media Format 4.0 profile. (Deprecated.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70d9a2e7-2f5a-4f87-b42c-3a225c42a44b">GetIndexMode</a>
</td>
<td align="left" width="63%">
Retrieves the current index mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7f5d13a-d36e-4da2-babc-0446e5697b61">SetIndexMode</a>
</td>
<td align="left" width="63%">
Enables the application to control whether the file will be indexed and therefore seekable.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>
 

 

