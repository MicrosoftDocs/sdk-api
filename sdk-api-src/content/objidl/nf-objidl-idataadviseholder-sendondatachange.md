---
UID: NF:objidl.IDataAdviseHolder.SendOnDataChange
title: IDataAdviseHolder::SendOnDataChange (objidl.h)
description: Sends notifications to each advise sink for which there is a connection established by calling the IAdviseSink::OnDataChange method for each advise sink currently being handled by this instance of the advise holder object.
helpviewer_keywords: ["IDataAdviseHolder interface [COM]","SendOnDataChange method","IDataAdviseHolder.SendOnDataChange","IDataAdviseHolder::SendOnDataChange","SendOnDataChange","SendOnDataChange method [COM]","SendOnDataChange method [COM]","IDataAdviseHolder interface","_ole_idataadviseholder_sendondatachange","com.idataadviseholder_sendondatachange","objidl/IDataAdviseHolder::SendOnDataChange"]
old-location: com\idataadviseholder_sendondatachange.htm
tech.root: com
ms.assetid: b7385116-2ec7-4e12-a2dc-c9029a38d8fd
ms.date: 12/05/2018
ms.keywords: IDataAdviseHolder interface [COM],SendOnDataChange method, IDataAdviseHolder.SendOnDataChange, IDataAdviseHolder::SendOnDataChange, SendOnDataChange, SendOnDataChange method [COM], SendOnDataChange method [COM],IDataAdviseHolder interface, _ole_idataadviseholder_sendondatachange, com.idataadviseholder_sendondatachange, objidl/IDataAdviseHolder::SendOnDataChange
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IDataAdviseHolder::SendOnDataChange
 - objidl/IDataAdviseHolder::SendOnDataChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IDataAdviseHolder.SendOnDataChange
---

# IDataAdviseHolder::SendOnDataChange


## -description

Sends notifications to each advise sink for which there is a connection established by calling the <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a> method for each advise sink currently being handled by this instance of the advise holder object.

## -parameters

### -param pDataObject [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data object in which the data has just changed. This pointer is used in subsequent calls to <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a>.

### -param dwReserved [in]

This parameter is reserved and must be 0.

### -param advf [in]

Container for advise flags that specify how the call to <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a> is made. These flag values are from the enumeration <a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a>. Typically, the value for <i>advf</i> is <b>NULL</b>. The only exception occurs when the data object is shutting down and must send a final notification that includes the actual data to sinks that have specified ADVF_DATAONSTOP and ADVF_NODATA in their call to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>. In this case, <i>advf</i> contains ADVF_DATAONSTOP.

## -returns

This method returns S_OK on success.

## -remarks

The data object must call this method when it detects a change that would be of interest to an advise sink that has previously requested notification.

Most notifications include the actual data with them. The only exception is if the ADVF_NODATA flag was previously specified when the connection was initially set up in the <a href="/windows/desktop/api/objidl/nf-objidl-idataadviseholder-advise">IDataAdviseHolder::Advise</a> method.

Before calling the <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a> method for each advise sink, this method obtains the actual data by calling the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> method through the pointer specified in the <i>pDataObject</i> parameter.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a>