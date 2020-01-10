---
UID: NN:tuner.ITuningSpace
title: ITuningSpace (tuner.h)
description: The ITuningSpace interface provides the common functionality for all network-specific tuning spaces.
old-location: mstv\ituningspace.htm
tech.root: mstv
ms.assetid: 51850105-b3b1-4758-acde-05ca2f3439f2
ms.date: 12/05/2018
ms.keywords: ITuningSpace, ITuningSpace interface [Microsoft TV Technologies], ITuningSpace interface [Microsoft TV Technologies],described, ITuningSpaceInterface, mstv.ituningspace, tuner/ITuningSpace
f1_keywords:
- tuner/ITuningSpace
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
- tuner.h
api_name:
- ITuningSpace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuningSpace interface


## -description



The <b>ITuningSpace</b> interface provides the common functionality for all network-specific tuning spaces. Applications can obtain tuning spaces from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/systemtuningspaces-object">SystemTuningSpaces</a> collection. A tuning space generally exposes an interface that inherits <b>ITuningSpace</b>, such as <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuningSpace</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-createtunerequest">CreateTuneRequest</a>
</td>
<td align="left" width="63%">
Creates a COM object representing an empty (uninitialized) tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-enumcategoryguids">EnumCategoryGUIDs</a>
</td>
<td align="left" width="63%">
(Currently not implemented.) Creates an enumerator for the DirectShow category GUIDs, representing classes of filters that support the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-enumdevicemonikers">EnumDeviceMonikers</a>
</td>
<td align="left" width="63%">
(Currently not implemented.) Creates an enumerator of device monikers representing the tuner inputs (filters) supporting this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get__networktype">get__NetworkType</a>
</td>
<td align="left" width="63%">
Retrieves the network type of the tuning space as a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_clsid">get_CLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID of the tuning space as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_defaultlocator">get_DefaultLocator</a>
</td>
<td align="left" width="63%">
Retrieves the default locator for a tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_defaultpreferredcomponenttypes">get_DefaultPreferredComponentTypes</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the preferred component types, which specify parameters such as the preferred audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_frequencymapping">get_FrequencyMapping</a>
</td>
<td align="left" width="63%">
Retrieves the frequency mapping previously created by the network provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_friendlyname">get_FriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the localized, user-friendly name of the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_networktype">get_NetworkType</a>
</td>
<td align="left" width="63%">
Retrieves the network type of the tuning space as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_uniquename">get_UniqueName</a>
</td>
<td align="left" width="63%">
Retrieves a unique name for the tuning space. Can be either a short name, or a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-put__networktype">put__NetworkType</a>
</td>
<td align="left" width="63%">
Sets the network type for this tuning space as a CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-put_defaultlocator">put_DefaultLocator</a>
</td>
<td align="left" width="63%">
Sets the default locator for a tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-put_defaultpreferredcomponenttypes">put_DefaultPreferredComponentTypes</a>
</td>
<td align="left" width="63%">
Creates an enumeration of the preferred component types, which specify parameters such as the preferred audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-put_frequencymapping">put_FrequencyMapping</a>
</td>
<td align="left" width="63%">
Creates a frequency/channel map, frequency/transponder map, or whatever other mapping from carrier frequencies to frequency identifiers is appropriate for the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-put_friendlyname">put_FriendlyName</a>
</td>
<td align="left" width="63%">
Sets the localized, user-friendly name of the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-put_networktype">put_NetworkType</a>
</td>
<td align="left" width="63%">
Sets the network type for this tuning space as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-put_uniquename">put_UniqueName</a>
</td>
<td align="left" width="63%">
Sets a unique name for the tuning space. Can be either a short name, or a GUID.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuningSpace)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

