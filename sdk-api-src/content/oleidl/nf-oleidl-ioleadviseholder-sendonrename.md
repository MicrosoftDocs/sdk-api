---
UID: NF:oleidl.IOleAdviseHolder.SendOnRename
title: IOleAdviseHolder::SendOnRename (oleidl.h)
description: Sends notification to all advisory sinks currently registered with the advise holder that the name of object has changed.
helpviewer_keywords: ["IOleAdviseHolder interface [COM]","SendOnRename method","IOleAdviseHolder.SendOnRename","IOleAdviseHolder::SendOnRename","SendOnRename","SendOnRename method [COM]","SendOnRename method [COM]","IOleAdviseHolder interface","_ole_ioleadviseholder_sendonrename","com.ioleadviseholder_sendonrename","oleidl/IOleAdviseHolder::SendOnRename"]
old-location: com\ioleadviseholder_sendonrename.htm
tech.root: com
ms.assetid: 64e44cab-b618-49af-bf0e-966b9eaa198a
ms.date: 12/05/2018
ms.keywords: IOleAdviseHolder interface [COM],SendOnRename method, IOleAdviseHolder.SendOnRename, IOleAdviseHolder::SendOnRename, SendOnRename, SendOnRename method [COM], SendOnRename method [COM],IOleAdviseHolder interface, _ole_ioleadviseholder_sendonrename, com.ioleadviseholder_sendonrename, oleidl/IOleAdviseHolder::SendOnRename
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IOleAdviseHolder::SendOnRename
 - oleidl/IOleAdviseHolder::SendOnRename
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleAdviseHolder.SendOnRename
---

# IOleAdviseHolder::SendOnRename


## -description

Sends notification to all advisory sinks currently registered with the advise holder that the name of object has changed.

## -parameters

### -param pmk [in]

A pointer to the new full moniker of the object.

## -returns

This method returns S_OK if advise sinks were sent <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onrename">IAdviseSink::OnRename</a> notifications.

## -remarks

<b>SendOnRename</b> calls <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onrename">IAdviseSink::OnRename</a> to advise the calling object, which must have already established an advisory connection, that the object has a new moniker. If you are using the OLE advise holder (having obtained a pointer through a call to <a href="/windows/desktop/api/ole2/nf-ole2-createoleadviseholder">CreateOleAdviseHolder</a>), you can call <b>SendOnRename</b> in the implementation of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a>, when you have determined that the operation is successful.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onrename">IAdviseSink::OnRename</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a>