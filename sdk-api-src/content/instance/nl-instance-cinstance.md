---
UID: NL:instance.CInstance
title: CInstance
author: windows-sdk-content
description: The CInstance class is used to retrieve and update the values of properties defined for the instances supported by the WMI Provider Framework. The CInstance class also provides access to the provider framework's implementation of the CInstance interface.
old-location: wmi\cinstance.htm
tech.root: WmiSdk
ms.assetid: aed29340-eb64-437d-b7e8-4f0e49c8288a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CInstance, CInstance class [Windows Management Instrumentation], CInstance class [Windows Management Instrumentation],described, _hmm_cinstance, instance/CInstance, wmi.cinstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: instance.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CInstance class


## -description


<p class="CCE_Message">[The <b>CInstance</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>CInstance</b> class is used to retrieve and update the values of properties defined for the instances supported by the WMI Provider Framework. The <b>CInstance</b> class also provides access to the provider framework's implementation of the <b>CInstance</b> interface.

It is not expected that provider writers will need to derive from this class. Use <a href="https://msdn.microsoft.com/cb520b55-9ef8-4f5a-935d-46c2bb01f5dd">Provider::CreateNewInstance</a> to create an instance of this class.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CInstance</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>CInstance</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/699dadf9-18b5-4c6d-a5c4-59ea8a85f089">Commit</a>
</td>
<td align="left" width="63%">
Returns the current instance to WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc8d0c91-03fb-4dc1-86a6-c1117f198181">Getbool</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a84b2de4-453d-4f69-8bac-df361180bc10">GetByte</a>
</td>
<td align="left" width="63%">
Retrieves a <b>BYTE</b>-compatible property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9295ba1-19da-41a2-86d1-ec80e18e895b">GetCHString</a>
</td>
<td align="left" width="63%">
Retrieves a string property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b5e5c14-c036-4ed5-8a47-9a67860e5585">GetClassObjectInterface</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7474d1c-4ed9-4669-a0e6-01230a3bf8fa">GetDateTime</a>
</td>
<td align="left" width="63%">
Returns a datetime property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39360e69-0d54-4b1f-8de8-0abf81e9238b">GetDOUBLE</a>
</td>
<td align="left" width="63%">
Retrieves a <b>DOUBLE</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02690232-a887-4de3-a850-84ad8ffa9ee0">GetDWORD</a>
</td>
<td align="left" width="63%">
Retrieves a <b>DWORD</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7daf313-d454-4e2c-8a8b-4f1bd9e19c58">GetEmbeddedObject</a>
</td>
<td align="left" width="63%">
Retrieves an embedded <b>CInstance</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2033754-4fd0-405f-9ad9-737eb8931016">GetMethodContext</a>
</td>
<td align="left" width="63%">
Returns a pointer to a <b>MethodContext</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/355386c5-7cd2-46de-8696-a83bd3f96cc5">GetStatus</a>
</td>
<td align="left" width="63%">
Determines whether a property exists and, if so, determines its type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7fc870a-952e-49a9-87ff-c191e4896511">GetStringArray</a>
</td>
<td align="left" width="63%">
Retrieves a property that represents an array of strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b14c7a62-579b-4a96-b018-c62918c9c35e">GetTimeSpan</a>
</td>
<td align="left" width="63%">
Retrieves a property that represents a WMI time span.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84160043-bb63-422b-99be-3f55df4c15be">GetVariant</a>
</td>
<td align="left" width="63%">
Retrieves a <b>VARIANT</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f22a939-58a9-4444-8d17-04330cded7d1">GetWBEMINT16</a>
</td>
<td align="left" width="63%">
Retrieves a 16-bit integer property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b51d0c51-3b72-4358-8fc3-d1dbc298b4d9">GetWBEMINT64</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves a 64-bit integer property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c2f3dfc-aa84-4dff-a25b-b8f2ec3afa74">GetWCHAR</a>
</td>
<td align="left" width="63%">
Retrieves a <b>WCHAR</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/511e4ce9-33e3-4c64-8016-05dd5630970f">GetWORD</a>
</td>
<td align="left" width="63%">
Retrieves a <b>WORD</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54d0135f-f387-43f5-ab5a-aa134141d3b0">IsNull</a>
</td>
<td align="left" width="63%">
Determines if the value of a particular property is <b>NULL</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4ca045d-a018-48a0-a4ea-94d0c8f094a6">Setbool</a>
</td>
<td align="left" width="63%">
Sets a <b>Boolean</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6ecbada-4eb6-40ad-9e59-ba77fd3b883a">SetByte</a>
</td>
<td align="left" width="63%">
Sets a <b>BYTE</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f59a2ea-3513-4a14-ac1a-62ed833d7192">SetCharSplat</a>
</td>
<td align="left" width="63%">Overloaded. Sets a string property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a75b574d-9ee7-4930-a003-5d71c5f1d687">SetCHString</a>
</td>
<td align="left" width="63%">Overloaded. Sets a string property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/728ad7d3-f56d-472e-976d-59d8598f3bad">SetDateTime</a>
</td>
<td align="left" width="63%">
Sets a datetime property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b6e2dcf-6feb-454a-a56a-79ae1506b4f9">SetDOUBLE</a>
</td>
<td align="left" width="63%">
Sets a <b>DOUBLE</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06b2ab13-b42d-4dfe-83f2-ecc526977b92">SetDWORD</a>
</td>
<td align="left" width="63%">
Sets a <b>DWORD</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64000949-8a3d-47c9-888b-09d520c41e1e">SetEmbeddedObject</a>
</td>
<td align="left" width="63%">
Sets an embedded <b>CInstance</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4157275a-cf71-4aca-ae86-0ae0b0e7fda7">SetNull</a>
</td>
<td align="left" width="63%">
Sets a property to <b>NULL</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcd1e108-4914-43ea-aa41-d38d38e8954a">SetStringArray</a>
</td>
<td align="left" width="63%">
Sets a property that represents an array of strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d23197a2-7352-44e8-b962-2509fdf9673d">SetTimeSpan</a>
</td>
<td align="left" width="63%">
Sets a property that represents a time span.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45201e64-2ecc-4a18-9f41-2392dfe50caf">SetVariant</a>
</td>
<td align="left" width="63%">
Sets a <b>VARIANT</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a39d3885-6344-4c05-8eea-da3f33fb998e">SetWBEMINT16</a>
</td>
<td align="left" width="63%">
Sets a 16-bit integer property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1789091-ddb6-44f7-bc02-82e7c0209bf9">SetWBEMINT64</a>
</td>
<td align="left" width="63%">Overloaded. Sets a 64-bit integer property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c565630-3626-4d60-9bd2-74c2218bec11">SetWCHARSplat</a>
</td>
<td align="left" width="63%">
Sets a <b>WCHAR</b> string property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e58b98d9-56c2-4e92-90ee-c9ff4fae9f8f">SetWORD</a>
</td>
<td align="left" width="63%">
Sets a <b>WORD</b> property.

</td>
</tr>
</table> 


## -remarks



The destructor for this class is <b>CInstance::~CInstance</b>.

Methods of the <b>CInstance</b> class are used to retrieve and set property values. Property data types are defined using CIM data types which can be seen in a .mof file. When querying or setting a property value using <b>CInstance</b> methods, it is necessary to use a method that is compatible with the property's CIM data type. The following table lists CIM data types and the permissible <b>CInstance</b> get or set methods for accessing a property of that data type.

<table>
<tr>
<th>CIM data type</th>
<th>CInstance Get/Set method types</th>
</tr>
<tr>
<td><b>string</b></td>
<td>

<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>


VARIANT

WCHAR

CharSplat

</td>
</tr>
<tr>
<td><b>sint8</b></td>
<td>
VARIANT

</td>
</tr>
<tr>
<td><b>uint8</b></td>
<td>
BYTE

</td>
</tr>
<tr>
<td><b>sint16</b></td>
<td>
WBEMINT16

VARIANT

</td>
</tr>
<tr>
<td><b>uint16</b></td>
<td>
WORD

DWORD

VARIANT

</td>
</tr>
<tr>
<td><b>sint32</b></td>
<td>
WORD

DWORD

VARIANT

</td>
</tr>
<tr>
<td><b>uint32</b></td>
<td>
WORD

DWORD

VARIANT

</td>
</tr>
<tr>
<td><b>sint64</b></td>
<td>

<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>


VARIANT

WBEMINT64

WCHAR

</td>
</tr>
<tr>
<td><b>uint64</b></td>
<td>

<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>


VARIANT

WBEMINT64

WCHAR

</td>
</tr>
<tr>
<td><b>real32</b></td>
<td>
VARIANT

</td>
</tr>
<tr>
<td><b>real64</b></td>
<td>

<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>


DOUBLE

VARIANT

</td>
</tr>
<tr>
<td><b>char16</b></td>
<td>VARIANT</td>
</tr>
<tr>
<td><b>DateTime</b></td>
<td>

<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>


DateTime

VARIANT

WCHAR

</td>
</tr>
</table>
 



