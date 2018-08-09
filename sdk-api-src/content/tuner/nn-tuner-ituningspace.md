---
UID: NN:tuner.ITuningSpace
title: ITuningSpace
author: windows-sdk-content
description: The ITuningSpace interface provides the common functionality for all network-specific tuning spaces.
old-location: mstv\ituningspace.htm
old-project: mstv
ms.assetid: 51850105-b3b1-4758-acde-05ca2f3439f2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITuningSpace, ITuningSpace interface [Microsoft TV Technologies], ITuningSpace interface [Microsoft TV Technologies],described, ITuningSpaceInterface, mstv.ituningspace, tuner/ITuningSpace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace interface


## -description



The <b>ITuningSpace</b> interface provides the common functionality for all network-specific tuning spaces. Applications can obtain tuning spaces from the <a href="https://msdn.microsoft.com/57cdd437-6219-4a72-96d9-642ff79d5879">SystemTuningSpaces</a> collection. A tuning space generally exposes an interface that inherits <b>ITuningSpace</b>, such as <a href="https://msdn.microsoft.com/313508e5-a9b2-42b8-bb2f-d191944d0939">IATSCTuningSpace</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuningSpace</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITuningSpace</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/513d4d3e-47df-4a12-80ce-9fc1400af176">CreateTuneRequest</a>
</td>
<td align="left" width="63%">
Creates a COM object representing an empty (uninitialized) tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9efbbda-fa95-46ea-aedc-7be5b13d16b5">EnumCategoryGUIDs</a>
</td>
<td align="left" width="63%">
(Currently not implemented.) Creates an enumerator for the DirectShow category GUIDs, representing classes of filters that support the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d1f9bcd-de94-4ea5-89a0-84042a514484">EnumDeviceMonikers</a>
</td>
<td align="left" width="63%">
(Currently not implemented.) Creates an enumerator of device monikers representing the tuner inputs (filters) supporting this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54cf0c5b-03fb-4419-976c-acc821dfc7e8">get__NetworkType</a>
</td>
<td align="left" width="63%">
Retrieves the network type of the tuning space as a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/def4aac2-3d0b-4ce6-9f6b-d13e7c3cc86d">get_CLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID of the tuning space as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/facc14bd-182e-4b8e-a567-1bf1d3c4ff36">get_DefaultLocator</a>
</td>
<td align="left" width="63%">
Retrieves the default locator for a tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a633a94c-e514-46b1-9982-7526ffa89b74">get_DefaultPreferredComponentTypes</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the preferred component types, which specify parameters such as the preferred audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86f6f991-7ba6-4dcc-86bd-03e44c799c22">get_FrequencyMapping</a>
</td>
<td align="left" width="63%">
Retrieves the frequency mapping previously created by the network provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1427aae-49e9-45ce-abd9-902a895e6e44">get_FriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the localized, user-friendly name of the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f264b6b3-98ae-44bc-8922-ab35c3b7a0d1">get_NetworkType</a>
</td>
<td align="left" width="63%">
Retrieves the network type of the tuning space as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c605f8c-7b0c-478d-a823-19e2f396953a">get_UniqueName</a>
</td>
<td align="left" width="63%">
Retrieves a unique name for the tuning space. Can be either a short name, or a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02e4ec53-e527-4cd2-a424-66c2f3fe4e43">put__NetworkType</a>
</td>
<td align="left" width="63%">
Sets the network type for this tuning space as a CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59065cc9-8a11-4551-ad3d-e7963628aa20">put_DefaultLocator</a>
</td>
<td align="left" width="63%">
Sets the default locator for a tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11ab6f15-1f16-42f9-9d7f-f0e51c83cba3">put_DefaultPreferredComponentTypes</a>
</td>
<td align="left" width="63%">
Creates an enumeration of the preferred component types, which specify parameters such as the preferred audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/665ab139-773c-4e02-896f-2f97063a786f">put_FrequencyMapping</a>
</td>
<td align="left" width="63%">
Creates a frequency/channel map, frequency/transponder map, or whatever other mapping from carrier frequencies to frequency identifiers is appropriate for the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97457657-9d28-4c8e-9db6-61271aa127e3">put_FriendlyName</a>
</td>
<td align="left" width="63%">
Sets the localized, user-friendly name of the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6af7062c-41c9-447f-8d92-bd67b8348933">put_NetworkType</a>
</td>
<td align="left" width="63%">
Sets the network type for this tuning space as a <b>BSTR</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44ce065b-5441-40c9-a987-6eafc04fba3d">put_UniqueName</a>
</td>
<td align="left" width="63%">
Sets a unique name for the tuning space. Can be either a short name, or a GUID.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuningSpace)</code>.




## -see-also




<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

