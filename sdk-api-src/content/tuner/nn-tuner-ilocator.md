---
UID: NN:tuner.ILocator
title: ILocator (tuner.h)
author: windows-sdk-content
description: The ILocator interface is implemented (through derived interfaces such as IATSCLocator) on Locator objects that contain tuning information about the tuning space.
old-location: mstv\ilocator.htm
tech.root: mstv
ms.assetid: 1d6c18f0-e7f1-4a1c-9edb-e4b66297becf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ILocator, ILocator interface [Microsoft TV Technologies], ILocator interface [Microsoft TV Technologies],described, ILocatorInterface, mstv.ilocator, tuner/ILocator
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
 - ILocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILocator interface


## -description



The <b>ILocator</b> interface is implemented (through derived interfaces such as <a href="https://msdn.microsoft.com/8ca7d50f-e7cc-4938-a2ed-fce5278b73fd">IATSCLocator</a>) on Locator objects that contain tuning information about the tuning space. This base interface is never used directly, but only through the derived interfaces that are specific for a given network type.

 Locator objects can be created dynamically by Guide Store Loaders that have the necessary information about the tuning space, or a default locator for a tuning space can be installed by the third party who installs the tuning space. In any case, applications never create or examine locators except in certain testing or debugging scenarios. All Locator objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILocator</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ILocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a1fd730-80b9-439b-aab2-069710aa3dfa">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the Locator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15f6d54c-81c8-40d3-937f-c54102f3a230">get_CarrierFrequency</a>
</td>
<td align="left" width="63%">
Gets the frequency of the RF signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aaa81a62-7e19-4d71-8378-77d6318a4e84">get_InnerFEC</a>
</td>
<td align="left" width="63%">
Gets the type of inner forward error correction (FEC) that is used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9600c31-9a95-4955-8f8c-542760631050">get_InnerFECRate</a>
</td>
<td align="left" width="63%">
Gets the inner FEC rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6aca60fa-ea8d-440d-a037-20537c25a105">get_Modulation</a>
</td>
<td align="left" width="63%">
Gets the modulation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d32937e1-0b8c-485e-8bd0-df15ab2ed373">get_OuterFEC</a>
</td>
<td align="left" width="63%">
Gets the type of outer FEC that is used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/550103a8-dcf9-4a52-817a-61a589de4299">get_OuterFECRate</a>
</td>
<td align="left" width="63%">
Gets the outer FEC rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/828967df-6ce1-4320-ae83-7bfaec79f8c7">get_SymbolRate</a>
</td>
<td align="left" width="63%">
Gets the quadrature phase-shift keying (QPSK) symbol rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74617c08-dabc-48d7-a9da-d1631d7df961">put_CarrierFrequency</a>
</td>
<td align="left" width="63%">
Sets the frequency of the RF signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ba6cfdf-2095-489c-a899-4b4305758ccb">put_InnerFEC</a>
</td>
<td align="left" width="63%">
Sets the type of inner FEC to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/009d1ddf-73ae-432b-adf2-a5a0067345fa">put_InnerFECRate</a>
</td>
<td align="left" width="63%">
Sets the inner FEC rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84a5b2ce-d26b-4ffc-b757-a799658f2b34">put_Modulation</a>
</td>
<td align="left" width="63%">
Sets the modulation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0aaa4d8e-e760-4e22-90fe-e5667fafa113">put_OuterFEC</a>
</td>
<td align="left" width="63%">
Sets the type of outer FEC to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fd3fa42-4ed6-459b-a6a2-23ed67832780">put_OuterFECRate</a>
</td>
<td align="left" width="63%">
Sets the outer FEC rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1eb91e22-b9b1-47dc-a2e4-cc64eeaacaaa">put_SymbolRate</a>
</td>
<td align="left" width="63%">
Sets the QPSK symbol rate.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ILocator)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

