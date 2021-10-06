---
UID: NL:instance.CInstance
title: CInstance (instance.h)
description: The CInstance class is used to retrieve and update the values of properties defined for the instances supported by the WMI Provider Framework. The CInstance class also provides access to the provider framework's implementation of the CInstance interface.
helpviewer_keywords: ["CInstance","CInstance class [Windows Management Instrumentation]","CInstance class [Windows Management Instrumentation]","described","_hmm_cinstance","instance/CInstance","wmi.cinstance"]
old-location: wmi\cinstance.htm
tech.root: wmi
ms.assetid: aed29340-eb64-437d-b7e8-4f0e49c8288a
ms.date: 12/05/2018
ms.keywords: CInstance, CInstance class [Windows Management Instrumentation], CInstance class [Windows Management Instrumentation],described, _hmm_cinstance, instance/CInstance, wmi.cinstance
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CInstance
 - instance/CInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance
---

# CInstance class


## -description

<p class="CCE_Message">[The <b>CInstance</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>CInstance</b> class is used to retrieve and update the values of properties defined for the instances supported by the WMI Provider Framework. The <b>CInstance</b> class also provides access to the provider framework's implementation of the <b>CInstance</b> interface.

It is not expected that provider writers will need to derive from this class. Use <a href="/windows/desktop/api/provider/nf-provider-provider-createnewinstance">Provider::CreateNewInstance</a> to create an instance of this class.

<b>CInstance</b> has these types of members:
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-commit">Commit</a>
</td>
<td align="left" width="63%">
Returns the current instance to WMI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getbool">Getbool</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getbyte">GetByte</a>
</td>
<td align="left" width="63%">
Retrieves a <b>BYTE</b>-compatible property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getchstring">GetCHString</a>
</td>
<td align="left" width="63%">
Retrieves a string property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getclassobjectinterface">GetClassObjectInterface</a>
</td>
<td align="left" width="63%">
Returns an <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> interface pointer.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getdatetime">GetDateTime</a>
</td>
<td align="left" width="63%">
Returns a datetime property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getdouble">GetDOUBLE</a>
</td>
<td align="left" width="63%">
Retrieves a <b>DOUBLE</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getdword">GetDWORD</a>
</td>
<td align="left" width="63%">
Retrieves a <b>DWORD</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getembeddedobject">GetEmbeddedObject</a>
</td>
<td align="left" width="63%">
Retrieves an embedded <b>CInstance</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getmethodcontext">GetMethodContext</a>
</td>
<td align="left" width="63%">
Returns a pointer to a <b>MethodContext</b> object.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Determines whether a property exists and, if so, determines its type.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getstringarray">GetStringArray</a>
</td>
<td align="left" width="63%">
Retrieves a property that represents an array of strings.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-gettimespan">GetTimeSpan</a>
</td>
<td align="left" width="63%">
Retrieves a property that represents a WMI time span.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getvariant">GetVariant</a>
</td>
<td align="left" width="63%">
Retrieves a <b>VARIANT</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getwbemint16">GetWBEMINT16</a>
</td>
<td align="left" width="63%">
Retrieves a 16-bit integer property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/WmiSdk/cinstance-getwbemint64">GetWBEMINT64</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves a 64-bit integer property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getwchar">GetWCHAR</a>
</td>
<td align="left" width="63%">
Retrieves a <b>WCHAR</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-getword">GetWORD</a>
</td>
<td align="left" width="63%">
Retrieves a <b>WORD</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-isnull">IsNull</a>
</td>
<td align="left" width="63%">
Determines if the value of a particular property is <b>NULL</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setbool">Setbool</a>
</td>
<td align="left" width="63%">
Sets a <b>Boolean</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setbyte">SetByte</a>
</td>
<td align="left" width="63%">
Sets a <b>BYTE</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/WmiSdk/cinstance-setcharsplat">SetCharSplat</a>
</td>
<td align="left" width="63%">Overloaded. Sets a string property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/WmiSdk/cinstance-setchstring">SetCHString</a>
</td>
<td align="left" width="63%">Overloaded. Sets a string property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setdatetime">SetDateTime</a>
</td>
<td align="left" width="63%">
Sets a datetime property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setdouble">SetDOUBLE</a>
</td>
<td align="left" width="63%">
Sets a <b>DOUBLE</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setdword">SetDWORD</a>
</td>
<td align="left" width="63%">
Sets a <b>DWORD</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setembeddedobject">SetEmbeddedObject</a>
</td>
<td align="left" width="63%">
Sets an embedded <b>CInstance</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setnull">SetNull</a>
</td>
<td align="left" width="63%">
Sets a property to <b>NULL</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setstringarray">SetStringArray</a>
</td>
<td align="left" width="63%">
Sets a property that represents an array of strings.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-settimespan">SetTimeSpan</a>
</td>
<td align="left" width="63%">
Sets a property that represents a time span.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setvariant">SetVariant</a>
</td>
<td align="left" width="63%">
Sets a <b>VARIANT</b> property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setwbemint16">SetWBEMINT16</a>
</td>
<td align="left" width="63%">
Sets a 16-bit integer property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/aa389221(v=vs.85)">SetWBEMINT64</a>
</td>
<td align="left" width="63%">Overloaded. Sets a 64-bit integer property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setwcharsplat">SetWCHARSplat</a>
</td>
<td align="left" width="63%">
Sets a <b>WCHAR</b> string property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/instance/nf-instance-cinstance-setword">SetWORD</a>
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

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>


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

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>


VARIANT

WBEMINT64

WCHAR

</td>
</tr>
<tr>
<td><b>uint64</b></td>
<td>

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>


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

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>


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

<a href="/windows/desktop/WmiSdk/chstring">CHString</a>


DateTime

VARIANT

WCHAR

</td>
</tr>
</table>
