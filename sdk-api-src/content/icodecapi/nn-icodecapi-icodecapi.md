---
UID: NN:icodecapi.ICodecAPI
title: ICodecAPI
ms.date: 08/05/2022
targetos: Windows
description:  The ICodecAPI interface sets and retrieves settings on an encoder or decoder filter, and defines a generic mechanism for setting properties on a codec.
helpviewer_keywords: ["ICodecAPI","ICodecAPI interface [DirectShow]","ICodecAPI interface [DirectShow]","described","ICodecAPIInterface","dshow.icodecapi","icodecapi/ICodecAPI"]
tech.root: mf
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: icodecapi.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - icodecapi.h
api_name:
 - ICodecAPI
f1_keywords:
 - ICodecAPI
 - icodecapi/ICodecAPI
dev_langs:
 - c++
---

## -description

The <b>ICodecAPI</b> interface sets and retrieves settings on an encoder or decoder filter.

## -remarks


This interface defines a generic mechanism for setting properties on a codec (encoder or decoder). A <i>codec property</i> is a key/value pair, where the key is a GUID and the value is a <b>VARIANT</b>. The interpretation of the <b>VARIANT</b> data depends on the property GUID. For a list of codec property GUIDs, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

<h3><a id="Codec_Profiles"></a><a id="codec_profiles"></a><a id="CODEC_PROFILES"></a>Codec Profiles</h3>
Codecs can optionally store profile and capability information in the system registry. This information enables applications to query the device during device enumeration. Default profiles are stored in the following registry key:<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Classes</b>
         <b>CLSID</b>
            <b><i>Category</i></b>
               <b>Profiles</b></pre>Each profile is a registry key whose default string is a text description of the profile. Each value has a GUID name, followed by a string value containing the numeric GUID value. For example:

<div class="code"><span><table>
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

<div class="code"><span><table>
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


<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>

