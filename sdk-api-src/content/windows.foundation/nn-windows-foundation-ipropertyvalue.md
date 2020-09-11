---
UID: NN:windows.foundation.IPropertyValue
title: IPropertyValue (windows.foundation.h)
description: Represents a value in a Windows Runtime property store.
helpviewer_keywords: ["IPropertyValue","IPropertyValue interface [Windows Runtime]","IPropertyValue interface [Windows Runtime]","described","windows/IPropertyValue","winrt.ipropertyvalue"]
old-location: winrt\ipropertyvalue.htm
tech.root: WinRT
ms.assetid: 447625BA-F982-4155-9B05-E478E1229443
ms.date: 12/05/2018
ms.keywords: IPropertyValue, IPropertyValue interface [Windows Runtime], IPropertyValue interface [Windows Runtime],described, windows/IPropertyValue, winrt.ipropertyvalue
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyValue
 - windows.foundation/IPropertyValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IPropertyValue
---

# IPropertyValue interface


## -description

Represents a value in a Windows Runtime property store.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyValue</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IPropertyValue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IPropertyValue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getboolean">GetBoolean</a>
</td>
<td align="left" width="63%">
Gets the 8-bit Boolean value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getbooleanarray">GetBooleanArray</a>
</td>
<td align="left" width="63%">
Gets the array of 8-bit Boolean values that is stored in the current  <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getchar16">GetChar16</a>
</td>
<td align="left" width="63%">
Gets the Unicode character that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getchar16array">GetChar16Array</a>
</td>
<td align="left" width="63%">
Gets the the array of Unicode characters that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getdatetime">GetDateTime</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a> value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getdatetimearray">GetDateTimeArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a> values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getdouble">GetDouble</a>
</td>
<td align="left" width="63%">
Gets the 64-bit floating point value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getdoublearray">GetDoubleArray</a>
</td>
<td align="left" width="63%">
Gets the array of 64-bit floating point values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getguid">GetGuid</a>
</td>
<td align="left" width="63%">
Gets the GUID value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getguidarray">GetGuidArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://docs.microsoft.com/dotnet/api/system.guid?redirectedfrom=MSDN">Guid</a> values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getinspectablearray">GetInspectableArray</a>
</td>
<td align="left" width="63%">
Gets the array of pointers to <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> objects that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getint32">GetInt32</a>
</td>
<td align="left" width="63%">
Gets the signed 32-bit integer value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getint32array">GetInt32Array</a>
</td>
<td align="left" width="63%">
Gets the array of signed 32-bit integer values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getint64">GetInt64</a>
</td>
<td align="left" width="63%">
Gets the signed 64-bit integer value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getint64array">GetInt64Array</a>
</td>
<td align="left" width="63%">
Gets the array of signed 64-bit integer values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getpoint">GetPoint</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a> value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getpointarray">GetPointArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a> values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getrect">GetRect</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a> value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getrectarray">GetRectArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a> values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getsingle">GetSingle</a>
</td>
<td align="left" width="63%">
Gets the 32-bit floating point value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getsinglearray">GetSingleArray</a>
</td>
<td align="left" width="63%">
Gets the array of 32-bit floating point values that is stored in the current <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-size">Size</a> value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getsizearray">GetSizeArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-size">Size</a> values that is stored in the current <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getstring">GetString</a>
</td>
<td align="left" width="63%">
Gets the string value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getstringarray">GetStringArray</a>
</td>
<td align="left" width="63%">
Gets the array of string values that is stored in the current <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-gettimespan">GetTimeSpan</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-timespan">TimeSpan</a> value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-gettimespanarray">GetTimeSpanArray</a>
</td>
<td align="left" width="63%">
Gets the array of <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-timespan">TimeSpan</a> values that is stored in the current <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getuint32">GetUInt32</a>
</td>
<td align="left" width="63%">
Gets the unsigned 32-bit integer value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getuint32array">GetUInt32Array</a>
</td>
<td align="left" width="63%">
Gets the array of unsigned 32-bit integer values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getuint64">GetUInt64</a>
</td>
<td align="left" width="63%">
Gets the unsigned 64-bit integer value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getuint64array">GetUInt64Array</a>
</td>
<td align="left" width="63%">
Gets the array of unsigned 64-bit integer values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getuint8">GetUInt8</a>
</td>
<td align="left" width="63%">
Gets the unsigned 8-bit integer value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getuint8array">GetUInt8Array</a>
</td>
<td align="left" width="63%">
Gets the array of unsigned 8-bit integer values that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyValue</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-get_type">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the data type of the value that is stored in the current <b>IPropertyValue</b> object.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ne-windows-foundation-propertytype">PropertyType</a>

