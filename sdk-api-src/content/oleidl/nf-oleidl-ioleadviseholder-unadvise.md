---
UID: NF:oleidl.IOleAdviseHolder.Unadvise
title: IOleAdviseHolder::Unadvise (oleidl.h)
description: Deletes a previously established advisory connection. (IOleAdviseHolder.Unadvise)
helpviewer_keywords: ["IOleAdviseHolder interface [COM]","Unadvise method","IOleAdviseHolder.Unadvise","IOleAdviseHolder::Unadvise","Unadvise","Unadvise method [COM]","Unadvise method [COM]","IOleAdviseHolder interface","_ole_ioleadviseholder_unadvise","com.ioleadviseholder_unadvise","oleidl/IOleAdviseHolder::Unadvise"]
old-location: com\ioleadviseholder_unadvise.htm
tech.root: com
ms.assetid: 620bc43f-dfc7-48b7-a574-ca7287ffa42f
ms.date: 12/05/2018
ms.keywords: IOleAdviseHolder interface [COM],Unadvise method, IOleAdviseHolder.Unadvise, IOleAdviseHolder::Unadvise, Unadvise, Unadvise method [COM], Unadvise method [COM],IOleAdviseHolder interface, _ole_ioleadviseholder_unadvise, com.ioleadviseholder_unadvise, oleidl/IOleAdviseHolder::Unadvise
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
 - IOleAdviseHolder::Unadvise
 - oleidl/IOleAdviseHolder::Unadvise
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
 - IOleAdviseHolder.Unadvise
---

# IOleAdviseHolder::Unadvise


## -description

Deletes a previously established advisory connection.

## -parameters

### -param dwConnection [in]

The value previously returned by <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-advise">IOleAdviseHolder::Advise</a> in <i>pdwConnection</i>.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwConnection</i> parameter does not represent a valid advisory connection.

</td>
</tr>
</table>

## -remarks

<b>IOleAdviseHolder::Unadvise</b> is intended to be used to implement <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">IOleObject::Unadvise</a> to delete an advisory connection. In general, you would use the OLE advise holder having obtained a pointer through a call to <a href="/windows/desktop/api/ole2/nf-ole2-createoleadviseholder">CreateOleAdviseHolder</a>.

Typically, containers call this method at shutdown or when an object is deleted. In certain cases, containers could call this method on objects that are running but not currently visible, as a way of reducing the overhead of maintaining multiple advisory connections.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-advise">IOleAdviseHolder::Advise</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-enumadvise">IOleAdviseHolder::EnumAdvise</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">IOleObject::Unadvise</a>
