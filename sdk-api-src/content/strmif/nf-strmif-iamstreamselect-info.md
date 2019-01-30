---
UID: NF:strmif.IAMStreamSelect.Info
title: IAMStreamSelect::Info
author: windows-sdk-content
description: The Info method retrieves information about a given stream.
old-location: dshow\iamstreamselect_info.htm
tech.root: DirectShow
ms.assetid: 9396d4fb-e06e-4b54-9601-fd443c81ff35
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMStreamSelect interface [DirectShow],Info method, IAMStreamSelect.Info, IAMStreamSelect::Info, IAMStreamSelectInfo, Info, Info method [DirectShow], Info method [DirectShow],IAMStreamSelect interface, dshow.iamstreamselect_info, strmif/IAMStreamSelect::Info
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMStreamSelect.Info
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMStreamSelect::Info


## -description



The <code>Info</code> method retrieves information about a given stream.




## -parameters




### -param lIndex [in]

Zero-based index of the stream.


### -param ppmt [out]

Address of a variable that receives a pointer to the stream's media type. This parameter is optional and can be <b>NULL</b>. If the value is non-<b>NULL</b>, the method returns a pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure. The caller must delete the structure, including the format block. (You can use the <a href="https://msdn.microsoft.com/970f6b2b-2bf5-418d-b4ae-637561cd6765">DeleteMediaType</a> function from the DirectShow base-class library.)


### -param pdwFlags [out]

Pointer to a variable that receives one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>This stream is disabled.</td>
</tr>
<tr>
<td>AMSTREAMSELECTINFO_ENABLED</td>
<td>The stream is enabled, and others in this group might be enabled too.</td>
</tr>
<tr>
<td>AMSTREAMSELECTINFO_EXCLUSIVE</td>
<td>This stream is the only enabled stream in the group.</td>
</tr>
</table>
 

This parameter is optional and can be <b>NULL</b>.


### -param plcid [out]

Pointer to a variable that receives a locale context (LCID) value. If the stream is associated with a particular locale, the LCID is returned in this variable. Otherwise, the variable receives the value zero. This parameter is optional and can be <b>NULL</b>.


### -param pdwGroup [out]

Pointer to a variable that receives the logical group with which the stream is associated. This parameter is optional and can be <b>NULL</b>.


### -param ppszName [out]

Address of a variable that receives a pointer to the stream name. The caller must free the returned string by calling the <b>CoTaskMemFree</b> function. This parameter is optional and can be <b>NULL</b>.


### -param ppObject [out]

Address of a variable that receives an <b>IUnknown</b> interface pointer. The method might return a pointer to a pin or filter associated with the stream, or it might return the value <b>NULL</b>. If the method returns a non-<b>NULL</b> value, the caller must release the <b>IUnknown</b> pointer.

Calling the <a href="https://msdn.microsoft.com/ac17a218-34a4-49aa-9b4d-cb34f3c2a5d3">IAMStreamSelect::Enable</a> method might invalidate the object returned by this method.

This parameter is optional and can be <b>NULL</b>.

The <a href="https://msdn.microsoft.com/abadf37f-2876-496d-90e7-77c3475a0064">MPEG-1 Stream Splitter</a>, <a href="https://msdn.microsoft.com/06704a5a-e7ae-4187-ae36-32512d951aaf">MPEG-2 Splitter</a>, and <a href="https://msdn.microsoft.com/9b09dd86-3c22-4565-82a0-106d5ca2e42d">SAMI (CC) Parser</a> filters return a pointer to the pin associated with the selected stream.


### -param ppUnk [out]

Address of a variable that receives an <b>IUnknown</b> interface pointer. The method might return a pointer to an interface that is specific to the stream, or it might return the value <b>NULL</b>. If the method returns a non-<b>NULL</b> value, the caller must release the <b>IUnknown</b> pointer. This parameter is optional and can be <b>NULL</b>.

The MPEG-1 Stream Splitter, MPEG-2 Splitter, and SAMI (CC) Parser filters all return the value <b>NULL</b>. Third party filters might return a pointer to a custom filter interface.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a305e91e-f506-4bd1-b4d4-7361df89e158">IAMStreamSelect Interface</a>
 

 

