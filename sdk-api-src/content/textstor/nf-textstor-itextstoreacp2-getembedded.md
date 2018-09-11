---
UID: NF:textstor.ITextStoreACP2.GetEmbedded
title: ITextStoreACP2::GetEmbedded
author: windows-sdk-content
description: Gets an embedded document.
old-location: tsf\itextstoreacp2_getembedded.htm
tech.root: TSF
ms.assetid: 42e67702-4056-4b29-97a9-441045b29338
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GUID_TS_SERVICE_ACCESSIBLE, GUID_TS_SERVICE_ACTIVEX, GUID_TS_SERVICE_DATAOBJECT, GetEmbedded, GetEmbedded method [Text Services Framework], GetEmbedded method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetEmbedded method, ITextStoreACP2.GetEmbedded, ITextStoreACP2::GetEmbedded, textstor/ITextStoreACP2::GetEmbedded, tsf.itextstoreacp2_getembedded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP2.GetEmbedded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoreACP2::GetEmbedded


## -description


Gets an embedded document.


## -parameters




### -param acpPos [in]

Contains the character position, within the document, from where the object is obtained.


### -param rguidService [in]

Contains a GUID value that defines the requested format of the obtained object. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GUID_TS_SERVICE_DATAOBJECT"></a><a id="guid_ts_service_dataobject"></a><dl>
<dt><b>GUID_TS_SERVICE_DATAOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The object should be obtained as an <a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a> object.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_TS_SERVICE_ACCESSIBLE"></a><a id="guid_ts_service_accessible"></a><dl>
<dt><b>GUID_TS_SERVICE_ACCESSIBLE</b></dt>
</dl>
</td>
<td width="60%">
The object should be obtained as an <a href="https://msdn.microsoft.com/en-us/library/Dd317981(v=VS.85).aspx">Accessible object</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_TS_SERVICE_ACTIVEX"></a><a id="guid_ts_service_activex"></a><dl>
<dt><b>GUID_TS_SERVICE_ACTIVEX</b></dt>
</dl>
</td>
<td width="60%">
The object should be obtained as an ActiveX object.

</td>
</tr>
</table>
 


### -param riid [in]

Specifies the interface type requested.


### -param ppunk [out]

Pointer to an <b>IUnknown</b> pointer that receives the requested interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application does not support embedded objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
<i>acpPos</i> is not within the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface type is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read-only lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOOBJECT</b></dt>
</dl>
</td>
<td width="60%">
There is no embedded object at <i>acpPos</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOSERVICE</b></dt>
</dl>
</td>
<td width="60%">
The service type specified in <i>rguidService</i> is unsupported.

</td>
</tr>
</table>
 




## -remarks



Use <a href="https://msdn.microsoft.com/82904a96-70ec-4ceb-a3c4-5d48c801a9ef">QueryInterface</a> to probe for appropriate interfaces. Prospective interfaces include those associated with embedded documents or controls such as <b>IOleObject</b> , <b>IDataObject</b> , <b>IViewObject</b> , <b>IPersistStorage</b> , <b>IOleCache</b> , or <b>IDispatch</b> .




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd317981(v=VS.85).aspx">Accessible Objects</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a>



<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>
 

 

