---
UID: NF:mpeg2data.ISectionList.Initialize
title: ISectionList::Initialize (mpeg2data.h)
author: windows-sdk-content
description: The Initialize method initializes the object. This method should be called once, immediately after creating the object. The IMpeg2Data::GetSection and IMpeg2Data::GetTable methods call this method internally, so typically an application will not call it.
old-location: mstv\isectionlist_initialize.htm
tech.root: mstv
ms.assetid: 196abb62-97f6-4961-b843-895ae35fedc4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISectionList interface [Microsoft TV Technologies],Initialize method, ISectionList.Initialize, ISectionList::Initialize, ISectionListInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],ISectionList interface, mpeg2data/ISectionList::Initialize, mstv.isectionlist_initialize
ms.topic: method
req.header: mpeg2data.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Mpeg2data.h
api_name:
 - ISectionList.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISectionList::Initialize


## -description



The <b>Initialize</b> method initializes the object. This method should be called once, immediately after creating the object. The <a href="https://msdn.microsoft.com/9fb0d10f-7f9a-452d-9725-546d372430bd">IMpeg2Data::GetSection</a> and <a href="https://msdn.microsoft.com/c76a9117-5dd7-46fc-8390-3f1ec80f6499">IMpeg2Data::GetTable</a> methods call this method internally, so typically an application will not call it.




## -parameters




### -param requestType [in]

Specifies the request type, as an <a href="https://msdn.microsoft.com/d1811cd5-3dda-48d1-a3b3-e4189e2622bb">MPEG_REQUEST_TYPE</a> value.


### -param pMpeg2Data [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.


### -param pContext [in]

Pointer to an <a href="https://msdn.microsoft.com/7a92e545-805b-4ce6-bbf1-397f7a5f6524">MPEG_CONTEXT</a> structure. This structure indicates the MPEG-2 source.


### -param pid [in]

Specifies a packet identifier (PID), indicating which packets in the transport stream are requested.


### -param tid [in]

Specifies a table identifier (TID), indicating which table sections to retrieve.


### -param pFilter [in]

Optional pointer to an <a href="https://msdn.microsoft.com/a7e66de7-d67b-4814-9849-076c3dd5afb1">MPEG2_FILTER</a> structure. The caller can use this parameter to exclude packets based on additional MPEG-2 header fields. This parameter can be <b>NULL</b>.


### -param timeout [in]

Specifies the maximum length of time that a synchronous request should wait before it times out.


### -param hDoneEvent [in]

Specifies a handle to an event. The object signals the event when the request completes. This parameter is optional; it should be specified for asynchronous requests.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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
<dt><b>MPEG2_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The object has already been initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method is either synchronous or asynchronous, depending on the request type defined in the <i>requestType</i> parameter. When the method is asynchronous, it returns immediately and signals the event specified in <i>hDoneEvent</i>. When the method is synchronous, it blocks until the request completes or until the time out specified in the <i>timeout</i> parameter expires.




## -see-also




<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList Interface</a>
 

 

