---
UID: NF:ocidl.IAdviseSinkEx.OnViewStatusChange
title: IAdviseSinkEx::OnViewStatusChange (ocidl.h)
description: Notifies the sink that a view status of an object has changed.
helpviewer_keywords: ["IAdviseSinkEx interface [COM]","OnViewStatusChange method","IAdviseSinkEx.OnViewStatusChange","IAdviseSinkEx::OnViewStatusChange","OnViewStatusChange","OnViewStatusChange method [COM]","OnViewStatusChange method [COM]","IAdviseSinkEx interface","_ole_iadvisesinkex_onviewstatuschange","com.iadvisesinkex_onviewstatuschange","ocidl/IAdviseSinkEx::OnViewStatusChange"]
old-location: com\iadvisesinkex_onviewstatuschange.htm
tech.root: com
ms.assetid: 9d5129aa-341c-4c69-8c0c-b7c3e62a57c1
ms.date: 12/05/2018
ms.keywords: IAdviseSinkEx interface [COM],OnViewStatusChange method, IAdviseSinkEx.OnViewStatusChange, IAdviseSinkEx::OnViewStatusChange, OnViewStatusChange, OnViewStatusChange method [COM], OnViewStatusChange method [COM],IAdviseSinkEx interface, _ole_iadvisesinkex_onviewstatuschange, com.iadvisesinkex_onviewstatuschange, ocidl/IAdviseSinkEx::OnViewStatusChange
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IAdviseSinkEx::OnViewStatusChange
 - ocidl/IAdviseSinkEx::OnViewStatusChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IAdviseSinkEx.OnViewStatusChange
---

# IAdviseSinkEx::OnViewStatusChange


## -description

Notifies the sink that a view status of an object has changed.

## -parameters

### -param dwViewStatus [in]

The new view status. Possible values are from the <a href="/windows/desktop/api/ocidl/ne-ocidl-viewstatus">VIEWSTATUS</a> enumeration.

## -returns

This method returns S_OK on success.

## -remarks

It is important that objects call the <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onviewchange">IAdviseSink:OnViewChange</a> method whenever the object's view changes even when the object is in place active. Containers rely on this notification to keep an object's view up-to-date.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onviewchange">IAdviseSink:OnViewChange</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iadvisesinkex">IAdviseSinkEx</a>