---
UID: NN:strmif.ICodecAPI
title: ICodecAPI
author: windows-sdk-content
description: The ICodecAPI interface sets and retrieves settings on an encoder or decoder filter.
old-location: dshow\icodecapi.htm
tech.root: DirectShow
ms.assetid: cc3f1bd9-1d36-45e6-94e2-07f2800fd073
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ICodecAPI, ICodecAPI interface [DirectShow], ICodecAPI interface [DirectShow],described, ICodecAPIInterface, dshow.icodecapi, strmif/ICodecAPI
ms.prod: windows
ms.technology: windows-sdk
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
---

# ICodecAPI interface


## -description



The <b>ICodecAPI</b> interface sets and retrieves settings on an encoder or decoder filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICodecAPI</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICodecAPI</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/45685033-73cc-4810-90f2-49343494641b">GetAllSettings</a>
</td>
<td align="left" width="63%">
Gets the codec's current settings and writes them to  a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/749f5235-2f62-4609-84b8-a880a38cd9cb">GetDefaultValue</a>
</td>
<td align="left" width="63%">
Retrieves the default value for a parameter, if one exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35bf758f-0ce3-4b3a-aae5-9d4326089743">GetParameterRange</a>
</td>
<td align="left" width="63%">
Returns the valid range of values for a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f6c7db8-f71f-4ea7-8584-0df6e28c0fc9">GetParameterValues</a>
</td>
<td align="left" width="63%">
Returns the list of supported values for a given parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/863ba518-c3c6-47d8-96d8-445a7e4d02aa">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the current value of a specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f7c7f72-02f2-4840-aaa2-9d26fe564577">IsModifiable</a>
</td>
<td align="left" width="63%">
Queries whether a parameter can be changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f556532-1a49-45c1-b446-89c05e8a8237">IsSupported</a>
</td>
<td align="left" width="63%">
Queries whether a given parameter is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87423ddb-7011-40ab-a449-eb43688efb26">RegisterForEvent</a>
</td>
<td align="left" width="63%">
Registers the application to receive a specified event from the encoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2f630be-a105-4f1b-9f9a-9d56c8853f35">SetAllDefaults</a>
</td>
<td align="left" width="63%">
Returns all parameters to their default values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f35845f-db62-466a-86cd-5788cdaa9809">SetAllDefaultsWithNotify</a>
</td>
<td align="left" width="63%">
Returns all parameters to their default values, and returns a list of the settings that have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1148e380-a4fc-4392-861e-8ea695060032">SetAllSettings</a>
</td>
<td align="left" width="63%">
Reads codec settings from a stream and sets them on the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30f840d1-4c73-4a76-ba0b-c04f2901ad76">SetAllSettingsWithNotify</a>
</td>
<td align="left" width="63%">
Loads encoder settings from a stream, sets them on the encoder, and returns a list of the settings that have changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e78a310a-3605-4cb3-a0c3-7864c890c1fa">SetValue</a>
</td>
<td align="left" width="63%">
Sets the value of a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2899e30-4dfb-47e7-88dd-adba49368a4f">SetValueWithNotify</a>
</td>
<td align="left" width="63%">
Sets the value of a parameter, and returns a list of other settings that have changed as a result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6f48379-664a-498f-8872-2272778588db">UnregisterForEvent</a>
</td>
<td align="left" width="63%">
Unregisters the application for a specified encoder event.

</td>
</tr>
</table> 


## -remarks



This interface defines a generic mechanism for setting properties on a codec (encoder or decoder). A <i>codec property</i> is a key/value pair, where the key is a GUID and the value is a <b>VARIANT</b>. The interpretation of the <b>VARIANT</b> data depends on the property GUID. For a list of codec property GUIDs, see <a href="https://msdn.microsoft.com/5d527af7-07cf-42e2-99bb-d56c856cc1bc">Codec API Properties</a>.

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




<a href="https://msdn.microsoft.com/019b063f-f215-44d8-a916-3125bee6af93">Decoder Settings for Windows Media Center Edition</a>



<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>
 

 

