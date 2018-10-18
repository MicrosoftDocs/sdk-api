---
UID: NN:dshowasf.IConfigAsfWriter
title: IConfigAsfWriter
author: windows-sdk-content
description: The IConfigAsfWriter interface is implemented by the DirectShow WM ASF Writer filter and provides methods for getting and setting the profiles and indexing mode.
old-location: wmformat\iconfigasfwriter.htm
tech.root: wmformat
ms.assetid: 481c0819-c18d-42e3-aebe-f156c414428d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IConfigAsfWriter, IConfigAsfWriter interface [windows Media Format], IConfigAsfWriter interface [windows Media Format],described, IConfigAsfWriterInterface, dshowasf/IConfigAsfWriter, wmformat.iconfigasfwriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Requires Dshowasf.h, Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dshowasf.h
api_name:
 - IConfigAsfWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAsfWriter interface


## -description



The <b>IConfigAsfWriter</b> interface is implemented by the DirectShow <a href="https://msdn.microsoft.com/a902c92e-836d-492c-b2d2-89c216125774">WM ASF Writer</a> filter and provides methods for getting and setting the profiles and indexing mode. The filter uses the profile to determine how many input pins to create, and what media types to accept at connection time. When the WM ASF Writer filter is first created, it is configured automatically with the following default profile: WMProfile_V80_256Video. (Use of this profile is not recommended because it does not use the Windows Media Audio and Video 9 Series codecs.)




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
<a href="https://msdn.microsoft.com/278e5109-ba22-4a1c-9c6a-5cfcb9f57d37">ConfigureFilterUsingProfile</a>
</td>
<td align="left" width="63%">
The recommended way to set a profile. Configures the filter to write an ASF file based on the specified application-defined profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94161ee7-1b74-47af-9d77-568abe6237c3">ConfigureFilterUsingProfileGuid</a>
</td>
<td align="left" width="63%">
Configures the filter to write an ASF file based on the specified predefined Windows Media Format SDK profile GUID. (Obsolete.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0375785-83db-4540-aca9-7ba0bb81c1ef">ConfigureFilterUsingProfileId</a>
</td>
<td align="left" width="63%">
Configures the filter to write an ASF file with a profile identifier (ID) index from the system profile list. (Obsolete. For Windows Media Format 4.0 profiles only.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f6e7085-982b-4234-b890-950efdcdb559">GetCurrentProfile</a>
</td>
<td align="left" width="63%">
Retrieves the application-defined profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7a2ecc0-48d4-446c-852a-0d7677cbbe71">GetCurrentProfileGuid</a>
</td>
<td align="left" width="63%">
Retrieves the current profile GUID defined by the Windows Media Format SDK.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5162bb1-5fcb-449e-b8d3-624b863e656d">GetCurrentProfileId</a>
</td>
<td align="left" width="63%">
Retrieves the current profile ID. (Deprecated. For Windows Media Format 4.0 profiles only.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/beb874ea-d0d5-4323-a817-47984911da4c">GetIndexMode</a>
</td>
<td align="left" width="63%">
Retrieves the current index mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2">SetIndexMode</a>
</td>
<td align="left" width="63%">
Enables the application to control whether the file will be indexed and therefore seekable.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/66f483b5-3886-48b4-bc43-7c3517abd20d">DirectShow QASF Reference</a>
 

 

