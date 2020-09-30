---
UID: NN:objidl.IStdMarshalInfo
title: IStdMarshalInfo (objidl.h)
description: Retrieves the CLSID identifying the handler to be used in the destination process during standard marshaling.
helpviewer_keywords: ["IStdMarshalInfo","IStdMarshalInfo interface [COM]","IStdMarshalInfo interface [COM]","described","_com_istdmarshalinfo","com.istdmarshalinfo","objidlbase/IStdMarshalInfo"]
old-location: com\istdmarshalinfo.htm
tech.root: com
ms.assetid: f034436f-e24e-4b99-9fb9-b0400d3ebb72
ms.date: 12/05/2018
ms.keywords: IStdMarshalInfo, IStdMarshalInfo interface [COM], IStdMarshalInfo interface [COM],described, _com_istdmarshalinfo, com.istdmarshalinfo, objidlbase/IStdMarshalInfo
req.header: objidl.h
req.include-header: ObjIdl.h
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
 - IStdMarshalInfo
 - objidl/IStdMarshalInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IStdMarshalInfo
---

# IStdMarshalInfo interface


## -description

Retrieves the CLSID identifying the handler to be used in the destination process during standard marshaling.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStdMarshalInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStdMarshalInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStdMarshalInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/objidl/nf-objidl-istdmarshalinfo-getclassforhandler">GetClassForHandler</a>
</td>
<td align="left" width="63%">
Retrieves the CLSID of the object handler to be used in the destination process during standard marshaling.

</td>
</tr>
</table>

## -remarks

An object that uses OLE's default implementation of <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> does not provide its own proxy but, by implementing <b>IStdMarshalInfo</b>, can nevertheless specify a handler to be loaded in the client process. Such a handler would typically handle certain requests in-process and use OLE's default marshaling to delegate others back to the original object.

To create an instance of an object in some client process, COM must first determine whether the object uses default marshaling or its own implementation. If the object uses default marshaling, COM then queries the object to determine whether it uses a special handler or, simply, OLE's default proxy. To get the CLSID of the handler to be loaded, COM queries the object for <b>IStdMarshalInfo</b> and then the <a href="/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a> interface. If neither interface is supported, a standard handler is used.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>