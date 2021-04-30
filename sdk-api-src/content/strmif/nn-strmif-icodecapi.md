---
UID: NN:strmif.ICodecAPI
title: ICodecAPI (strmif.h)
description: The ICodecAPI interface sets and retrieves settings on an encoder or decoder filter.
helpviewer_keywords: ["ICodecAPI","ICodecAPI interface [DirectShow]","ICodecAPI interface [DirectShow]","described","ICodecAPIInterface","dshow.icodecapi","strmif/ICodecAPI"]
old-location: dshow\icodecapi.htm
tech.root: dshow
ms.assetid: cc3f1bd9-1d36-45e6-94e2-07f2800fd073
ms.date: 12/05/2018
ms.keywords: ICodecAPI, ICodecAPI interface [DirectShow], ICodecAPI interface [DirectShow],described, ICodecAPIInterface, dshow.icodecapi, strmif/ICodecAPI
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICodecAPI
 - strmif/ICodecAPI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICodecAPI
---

# ICodecAPI interface


## -description

The <b>ICodecAPI</b> interface sets and retrieves settings on an encoder or decoder filter.

> [!Note]
> APIs declared in strmif.h are not supported for Universal Windows Platform (UWP) apps. To use ICodecAPI in a UWP app, use the version declared in [icodecapi.h](/windows/win32/api/icodecapi/). 

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICodecAPI</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICodecAPI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

This interface defines a generic mechanism for setting properties on a codec (encoder or decoder). A <i>codec property</i> is a key/value pair, where the key is a GUID and the value is a <b>VARIANT</b>. The interpretation of the <b>VARIANT</b> data depends on the property GUID. For a list of codec property GUIDs, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

<h3><a id="Codec_Profiles"></a><a id="codec_profiles"></a><a id="CODEC_PROFILES"></a>Codec Profiles</h3>
Codecs can optionally store profile and capability information in the system registry. This information enables applications to query the device during device enumeration. Default profiles are stored in the following registry key:<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Classes</b>
         <b>CLSID</b>
            <b><i>Category</i></b>
               <b>Profiles</b></pre>Each profile is a registry key whose default string is a text description of the profile. Each value has a GUID name, followed by a string value containing the numeric GUID value. For example:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
  HLKM\Software\Classes\CLSID\&lt;category&gt;\Profiles\DVD
    default "HQ DVD"
    REG_SZ {...} = "0"
    REG_SZ {...} = "1234"
</pre>
</td>
</tr>
</table></span></div>
where {...} is a property GUID that the application can map into its user interface. Microsoft is currently considering the definition of a set of standard profiles.

Default codec capabilities are stored under HLKM\Software\Classes\CLSID\&lt;category&gt;\Instance\&lt;Filter CLSID&gt;\Capabilities. Each value has a GUID name, followed by a string value containing the numeric GUID value. For example:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HLKM\Software\Classes\CLSID\&lt;category&gt;\Instance\&lt;My DVD encoder&gt;\Capabilities
     default "My DVD encoder"
     REG_SZ_MULTI {...}
</pre>
</td>
</tr>
</table></span></div>
where {...} is a property GUID that the application can map into its user interface.

## -see-also

<a href="/windows/desktop/DirectShow/decoder-settings-for-windows-media-center-edition">Decoder Settings for Windows Media Center Edition</a>



<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>
