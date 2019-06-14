---
UID: NN:mfobjects.IMFPluginControl
title: IMFPluginControl (mfobjects.h)
author: windows-sdk-content
description: Controls how media sources and transforms are enumerated in Microsoft Media Foundation.
old-location: mf\imfplugincontrol.htm
tech.root: medfound
ms.assetid: cdc6fd4f-c544-43bb-ba99-5468ef49949d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFPluginControl, IMFPluginControl interface [Media Foundation], IMFPluginControl interface [Media Foundation],described, mf.imfplugincontrol, mfobjects/IMFPluginControl
ms.topic: interface
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - mfobjects.h
api_name:
 - IMFPluginControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPluginControl interface


## -description


Controls how media sources and transforms are enumerated in Microsoft Media Foundation.

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfgetplugincontrol">MFGetPluginControl</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPluginControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPluginControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPluginControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-getdisabledbyindex">GetDisabledByIndex</a>
</td>
<td align="left" width="63%">
Gets a class identifier (CLSID) from the blocked list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-getpreferredclsid">GetPreferredClsid</a>
</td>
<td align="left" width="63%">
Searches the preferred list for a CLSID that matches a specified key name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-getpreferredclsidbyindex">GetPreferredClsidByIndex</a>
</td>
<td align="left" width="63%">
Gets a CLSID from the preferred list, specified by index value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-isdisabled">IsDisabled</a>
</td>
<td align="left" width="63%">
Queries whether a CLSID appears in the blocked list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-setdisabled">SetDisabled</a>
</td>
<td align="left" width="63%">
Adds a CLSID to the blocked list or removes a CLSID from the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-setpreferredclsid">SetPreferredClsid</a>
</td>
<td align="left" width="63%">
Adds a CLSID to the preferred list or removes a CLSID from the list.

</td>
</tr>
</table> 


## -remarks



Media Foundation provides a set of built-in media sources and decoders. Applications can enumerate them as follows: 

<ul>
<li>Media sources are enumerated through the <a href="https://docs.microsoft.com/windows/desktop/medfound/source-resolver">Source Resolver</a>.</li>
<li>Transforms, such as decoders, are enumerated through the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftenum">MFTEnum</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> functions.</li>
</ul>
Applications might also enumerate these objects indirectly. For example, if an application   uses the topology loader to resolve a partial topology, the topology loader calls <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> to find the required decoders.

Third parties can implement their own custom media sources and decoders, and register them for enumeration so that other applications can use them.

To control the enumeration order, Media Foundation maintains two process-wide lists of CLSIDs: a preferred list and a blocked list.  An object whose CLSID appears in the preferred list appears first in the enumeration order. An object whose CLSID appears on the blocked list is not enumerated.

The lists are initially populated from the registry. Applications can use the <b>IMFPluginControl</b> interface to modify the lists for the current process.

The preferred list contains a set of key/value pairs, where the keys are strings and the values are CLSIDs. These key/value pairs are defined as follows:

<ul>
<li>For media sources, the key name is a file name extension, protocol scheme, or MIME type. The value is the CLSID of a scheme handler or byte-stream handler for that media source.</li>
<li>For decoders, the key name is a media subtype GUID in canonical string form. (For more information about media subtypes, see <a href="https://docs.microsoft.com/windows/desktop/medfound/media-types">Media Types</a>.) The value is the CLSID of the Media Foundation transform (MFT) that implements the decoder. </li>
</ul>
The following examples show the various types of key:

<ul>
<li>File extension: ".wmv"</li>
<li>Scheme: "http:"</li>
<li>MIME type: "video/mp4"</li>
<li>Media subtype: "{47504A4D-0000-0010-8000-00AA00389B71}"</li>
</ul>
To search the preferred list by key name, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-getpreferredclsid">IMFPluginControl::GetPreferredClsid</a> method. To enumerate the entire list, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-getpreferredclsidbyindex">IMFPluginControl::GetPreferredClsidByIndex</a> method in a loop.

The blocked list contains a list of CLSIDs. To enumerate the entire list, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-getdisabledbyindex">IMFPluginControl::GetDisabledByIndex</a> method in a loop. To check whether a specific CLSID appears on the list, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol-isdisabled">IMFPluginControl::IsDisabled</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfgetplugincontrol">MFGetPluginControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

