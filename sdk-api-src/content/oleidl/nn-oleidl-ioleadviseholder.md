---
UID: NN:oleidl.IOleAdviseHolder
title: IOleAdviseHolder (oleidl.h)
author: windows-sdk-content
description: Manages advisory connections and compound document notifications in an object server.
old-location: com\ioleadviseholder.htm
tech.root: com
ms.assetid: 680afee7-2bee-4d54-ae0b-3e4e0deb622f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOleAdviseHolder, IOleAdviseHolder interface [COM], IOleAdviseHolder interface [COM],described, _ole_ioleadviseholder, com.ioleadviseholder, oleidl/IOleAdviseHolder
ms.topic: interface
f1_keywords: 
 - "oleidl/IOleAdviseHolder"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleAdviseHolder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleAdviseHolder interface


## -description


Manages advisory connections and compound document notifications in an object server. Its methods are intended to be used to implement the advisory methods of <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>. <b>IOleAdviseHolder</b> is implemented on an advise holder object. Its methods establish and delete advisory connections from the object managed by the server to the object's container, which must contain an advise sink (support the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> interface). The advise holder object must also keep track of which advise sinks are interested in which notifications and pass along the notifications as appropriate.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleAdviseHolder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleAdviseHolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleAdviseHolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-advise">Advise</a>
</td>
<td align="left" width="63%">
Establishes an advisory connection between an OLE object and the calling object's advise sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-enumadvise">EnumAdvise</a>
</td>
<td align="left" width="63%">
Creates an enumerator that can be used to enumerate the advisory connections currently established for an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-sendonclose">SendOnClose</a>
</td>
<td align="left" width="63%">
Sends notification to all advisory sinks currently registered with the advise holder that the object has closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-sendonrename">SendOnRename</a>
</td>
<td align="left" width="63%">
Sends notification to all advisory sinks currently registered with the advise holder that the name of object has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-sendonsave">SendOnSave</a>
</td>
<td align="left" width="63%">
Sends notification to all advisory sinks currently registered with the advise holder that the object has been saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Deletes a previously established advisory connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-createoleadviseholder">CreateOleAdviseHolder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>
 

 

