---
UID: NF:mpeg2data.ISectionList.Initialize
title: ISectionList::Initialize (mpeg2data.h)
description: The Initialize method initializes the object. This method should be called once, immediately after creating the object. The IMpeg2Data::GetSection and IMpeg2Data::GetTable methods call this method internally, so typically an application will not call it.
helpviewer_keywords: ["ISectionList interface [Microsoft TV Technologies]","Initialize method","ISectionList.Initialize","ISectionList::Initialize","ISectionListInitialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","ISectionList interface","mpeg2data/ISectionList::Initialize","mstv.isectionlist_initialize"]
old-location: mstv\isectionlist_initialize.htm
tech.root: mstv
ms.assetid: 196abb62-97f6-4961-b843-895ae35fedc4
ms.date: 12/05/2018
ms.keywords: ISectionList interface [Microsoft TV Technologies],Initialize method, ISectionList.Initialize, ISectionList::Initialize, ISectionListInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],ISectionList interface, mpeg2data/ISectionList::Initialize, mstv.isectionlist_initialize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISectionList::Initialize
 - mpeg2data/ISectionList::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - ISectionList.Initialize
---

# ISectionList::Initialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Initialize</b> method initializes the object. This method should be called once, immediately after creating the object. The <a href="/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2data-getsection">IMpeg2Data::GetSection</a> and <a href="/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2data-gettable">IMpeg2Data::GetTable</a> methods call this method internally, so typically an application will not call it.

## -parameters

### -param requestType [in]

Specifies the request type, as an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ne-mpeg2structs-mpeg_request_type">MPEG_REQUEST_TYPE</a> value.

### -param pMpeg2Data [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.

### -param pContext [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_context">MPEG_CONTEXT</a> structure. This structure indicates the MPEG-2 source.

### -param pid [in]

Specifies a packet identifier (PID), indicating which packets in the transport stream are requested.

### -param tid [in]

Specifies a table identifier (TID), indicating which table sections to retrieve.

### -param pFilter [in]

Optional pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg2_filter">MPEG2_FILTER</a> structure. The caller can use this parameter to exclude packets based on additional MPEG-2 header fields. This parameter can be <b>NULL</b>.

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

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList Interface</a>