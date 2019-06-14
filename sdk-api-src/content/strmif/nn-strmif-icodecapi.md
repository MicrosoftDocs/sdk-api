---
UID: NN:strmif.ICodecAPI
title: ICodecAPI (strmif.h)
author: windows-sdk-content
description: The ICodecAPI interface sets and retrieves settings on an encoder or decoder filter.
old-location: dshow\icodecapi.htm
tech.root: DirectShow
ms.assetid: cc3f1bd9-1d36-45e6-94e2-07f2800fd073
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICodecAPI, ICodecAPI interface [DirectShow], ICodecAPI interface [DirectShow],described, ICodecAPIInterface, dshow.icodecapi, strmif/ICodecAPI
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICodecAPI interface


## -description



The <b>ICodecAPI</b> interface sets and retrieves settings on an encoder or decoder filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICodecAPI</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICodecAPI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICodecAPI</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-getallsettings">GetAllSettings</a>
</td>
<td align="left" width="63%">
Gets the codec's current settings and writes them to  a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue">GetDefaultValue</a>
</td>
<td align="left" width="63%">
Retrieves the default value for a parameter, if one exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange">GetParameterRange</a>
</td>
<td align="left" width="63%">
Returns the valid range of values for a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-getparametervalues">GetParameterValues</a>
</td>
<td align="left" width="63%">
Returns the list of supported values for a given parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the current value of a specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-ismodifiable">IsModifiable</a>
</td>
<td align="left" width="63%">
Queries whether a parameter can be changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-issupported">IsSupported</a>
</td>
<td align="left" width="63%">
Queries whether a given parameter is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-registerforevent">RegisterForEvent</a>
</td>
<td align="left" width="63%">
Registers the application to receive a specified event from the encoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-setalldefaults">SetAllDefaults</a>
</td>
<td align="left" width="63%">
Returns all parameters to their default values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-setalldefaultswithnotify">SetAllDefaultsWithNotify</a>
</td>
<td align="left" width="63%">
Returns all parameters to their default values, and returns a list of the settings that have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-setallsettings">SetAllSettings</a>
</td>
<td align="left" width="63%">
Reads codec settings from a stream and sets them on the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-setallsettingswithnotify">SetAllSettingsWithNotify</a>
</td>
<td align="left" width="63%">
Loads encoder settings from a stream, sets them on the encoder, and returns a list of the settings that have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue">SetValue</a>
</td>
<td align="left" width="63%">
Sets the value of a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-setvaluewithnotify">SetValueWithNotify</a>
</td>
<td align="left" width="63%">
Sets the value of a parameter, and returns a list of other settings that have changed as a result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-icodecapi-unregisterforevent">UnregisterForEvent</a>
</td>
<td align="left" width="63%">
Unregisters the application for a specified encoder event.

</td>
</tr>
</table> 


## -remarks



This interface defines a generic mechanism for setting properties on a codec (encoder or decoder). A <i>codec property</i> is a key/value pair, where the key is a GUID and the value is a <b>VARIANT</b>. The interpretation of the <b>VARIANT</b> data depends on the property GUID. For a list of codec property GUIDs, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/decoder-settings-for-windows-media-center-edition">Decoder Settings for Windows Media Center Edition</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/encoder-api">Encoder API</a>
 

 

